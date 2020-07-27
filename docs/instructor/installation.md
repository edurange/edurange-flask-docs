## EDURange Installation

This is a step by step walkthrough for instructors on how to install the EDURange application on the Ubuntu operating system.

 1. If you have not already, install pip3 using 
 		`sudo apt install python3-pip`

 2. If you have not already, install git using 
 		`sudo apt install git`

 3. Clone the Github repository using 
 		`git clone https://github.com/coojac09/edurange-flask.git`

 4. Change directories to the applications root directory using 
 		`ch edurange-flask`

 5. Install the applications requirements using 
 		`pip3 install -r requirements/dev.txt`

 6. Make sure the application is on your path using 
 		`export PATH=$PATH : /home/$(whoami)/.local/bin`

 7. Install npm using 
 		`sudo apt install npm`

 8. Install npm to be able to run npm using 
 		`npm install`

 9. Install the redis server using 
 		`sudo apt install redis-server`

 10. Get a copy of the `.env` file. Currently the only way to do this is by contacting an EDURange administrator.

 11. Edit the credentials for the default admin. Be careful in doing so, as this will be your admin account on the application.

 12. Install the postgres server using 
 		`sudo apt install postgresql libpq-dev`

 13. Open the postgres command line using 
 		`sudo -u postgres psql`

 14. Change the default user using 
 		`ALTER USER postgres WITH PASSWORD 'passwordfoo';`

 15. Create the postgres database using 
 		`CREATE DATABASE refactor;`

 16. Exit the postgres command line using 
 		`\q`

 17. Make the data/tmp directories using 
 		`mkdir data`
 		`mkdir data/tmp`

 18. If you have not already, install unzip using 
 		`sudo apt install unzip`

 19. Download terraform from the terraform website using
 		`wget https://releases.hashicorp.com/terraform/0.12.29/terraform_0.12.29_linux_amd64.zip`

 20. Unzip the downloaded folder using
 		`unzip terraform_0.12.29_linux_amd64.zip`

 21. Move the terraform folder to `/usr/bin/terraform` using
 		`sudo mv terraform /usr/bin/terraform`

 22. Download docker from the docker website using
 		`wget get.docker.com`

 23. Rename the downloaded index.html using
 		`mv index.html docker.sh`

 24. Make docker.sh an executable using
 		`chmod +x docker.sh`

 25. Run docker.sh using
 		`./docker.sh`

 26. Run the application from the `edurange-flask` directory using
 		`npm start`

Upon running `npm start` the application should start running showing you a log of the applications activities with their related services highlighted. Webpack should be blue, Flask should be purple, and Celery should be green.

The application webpage can now be accessed by going to `127.0.0.1:5000` using your preferred web browser. You can log in with the default admin credentials that you set in the `.env` file. To stop the application simply go to the terminal showing the application activity log and press `Ctrl + C`.
