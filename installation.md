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
	
	`git clone https://github.com/coojac09/edurange-flask.git`

3. Change directories to the applications root directory using 
 	
	`cd edurange-flask`

4. Install the applications requirements using 
 	
	`pip3 install -r requirements/dev.txt`

5. Make sure the application is on your path using 
 	
	`export PATH=$PATH : /home/$(whoami)/.local/bin`

6. Prepare npm to run using
	
	`npm install`

7. Rename the `.env.example` file to `.env`

8. Edit the sections marked by the comments, namely the secret key and the default admin login credentials. The email server information is technically optional, but the account recovery/reset password functionality will be broken unless a valid email account and server are specified.

9. Make the data/tmp directories using:
 	
	-`mkdir data`
 	
	-`mkdir data/tmp`

---

#### Setting Up the Postgres Server

10. Open the postgres command line using 
 	
	`sudo -u postgres psql`

11. Change the default user using 
 	
	`ALTER USER postgres WITH PASSWORD 'passwordfoo';`

12. Create the postgres database using 
 	
	`CREATE DATABASE refactor;`

13. Exit the postgres command line using 
 	
	`\q`

> It should be noted that the database user password and the database name can be personalized but the `.env` file will need to be changed to match.

---

#### Setting Up Terraform

14. Download terraform from the terraform website using
 	
	`wget https://releases.hashicorp.com/terraform/0.12.29/terraform_0.12.29_linux_amd64.zip`

15. Unzip the downloaded folder using
	
	`unzip terraform_0.12.29_linux_amd64.zip`

16. Move the terraform folder to `/usr/bin/terraform` using
	
	`sudo mv terraform /usr/bin/terraform`

---

#### Setting Up Docker

17. Download docker from the docker website using
	
	`wget get.docker.com`

18. Rename the downloaded index.html using
	
	`mv index.html docker.sh`

19. Make docker.sh an executable using
	
	`chmod +x docker.sh`

20. Run docker.sh using
	
	`./docker.sh`

---

21. Run the application from the `edurange-flask` directory using
	
	`npm start`

Upon running `npm start` the application should start running showing you a log of the applications activities with their related services highlighted. Webpack should be blue, Flask should be purple, and Celery should be green.

The application webpage can now be accessed by going to `127.0.0.1:5000` using your preferred web browser. You can log in with the default admin credentials that you set in the `.env` file. To stop the application simply go to the terminal showing the application activity log and press `Ctrl + C`.
