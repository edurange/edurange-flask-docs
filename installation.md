## EDURange Installation

This is a step by step walkthrough for instructors on how to install the EDURange application on the Ubuntu operating system.


1. If you have not already please run the following intallation commands:
	
	-`sudo apt install git`

	-`sudo apt install python3-pip`

	-`sudo apt install npm`

	-`sudo apt install redis-server`

	-`sudo apt install unzip`

	-`sudo apt install postgresql libpq-dev`


2. Clone the Github repository using
	
	`git clone https://github.com/edurange/edurange-flask.git`

3. Change directories to the applications root directory using 
 	
	`cd edurange-flask`

4. Install the applications requirements using 
 	
	`pip3 install -r requirements/dev.txt`

5. Make sure the application is on your path using 
 	
	`export PATH=$PATH:/home/$(whoami)/.local/bin`

6. Prepare npm to run using
	
	`npm install`

7. Rename the `.env.example` file to `.env`

8. Edit the sections marked by the comments, namely the secret key and the default admin login credentials. The email server information is technically optional, but the account recovery/reset password functionality will be broken unless a valid email account and server are specified.

9. Make the data/tmp directories using:
 	
	-`mkdir data`
 	
	-`mkdir data/tmp`

10. Make the logs directory using
	
	`mkdir logs`

---

#### Setting Up the Postgres Server

11. Open the postgres command line using 
 	
	`sudo -u postgres psql`

12. Change the default user using 
 	
	`ALTER USER postgres WITH PASSWORD 'passwordfoo';`

13. Create the postgres database using 
 	
	`CREATE DATABASE refactor;`

14. Exit the postgres command line using 
 	
	`\q`

> It should be noted that the database user password and the database name can be personalized but the `.env` file will need to be changed to match.

---

#### Setting Up Terraform

15. Download terraform from the terraform website using
 	
	`wget https://releases.hashicorp.com/terraform/0.12.29/terraform_0.12.29_linux_amd64.zip`

16. Unzip the downloaded folder using
	
	`unzip terraform_0.12.29_linux_amd64.zip`

17. Move the terraform folder to `/usr/bin/terraform` using
	
	`sudo mv terraform /usr/bin/terraform`

---

#### Setting Up Docker

18. Download docker from the docker website using
	
	`wget get.docker.com`

19. Rename the downloaded index.html using
	
	`mv index.html docker.sh`

20. Make docker.sh an executable using
	
	`chmod +x docker.sh`

21. Run docker.sh using
	
	`./docker.sh`

> Please note that to run docker the user on the host machine must have access to the Docker bash command. You can test this by entering `docker run hello-world` into the command line.

22. Create the docker group and add your user to it using

	`sudo groupadd docker`

	`sudo usermod -aG docker ${USER}`

	> `${USER}` may need to be replaced with your username if bash is not able to recognize it as a variable.

---

23. Run the application from the `edurange-flask` directory using
	
	`npm start`


> Optionaly if administrators would like the application to be accessible on port 80 instead of port 5000, the following iptables rules can be executed
>	`sudo iptables -t nat -A OUTPUT -o lo -p tcp --dport 80 -j REDIRECT --to-port 5000`
>	`sudo iptables -t nat -A PREROUTING -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 5000`

Upon running `npm start` the application should start running showing you a log of the applications activities with their related services highlighted. Webpack should be blue, Flask should be purple, and Celery should be green.

The application webpage can now be accessed by going to `127.0.0.1:5000` using your preferred web browser. You can log in with the default admin credentials that you set in the `.env` file. To stop the application simply go to the terminal showing the application activity log and press `Ctrl + C`.


> Known issue:
> The first time the server is launched after resetting the database, there may be an "SQLKeyIntegrityError". This is from the admin user creation, restarting npm and refreshing the page should fix it, and it should never appear again.

