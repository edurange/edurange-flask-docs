## EDURange Installation

This is a step by step walkthrough for instructors on how to install the EDURange application. It should be noted that EDURange is a Python 3 based project, and that errors may arise if Python 2 is used.

Before installing the application please make sure that the Postgresql is installed and the database you intend to use for the application has been created.

 1. Go to the [Github repository](https://github.com/coojac09/edurange-flask) and clone the repository.

 2. Copy the `.env` file given to you by an EDURange administrator into the same directory as `autoapp.py`, and personalize the default admin fields in the .env file.

 3. In the same directory as `autoapp.py` run the following commands:
 	```bash
 	pip install -r requirements/dev.txt
 	npm install
 	npm start
 	```
 	Upon running `npm start` you should see a log of the applications activities, with their related packages highlighted. Webpack should be blue, Flask should be purple, and Celery should be green.

 4. The EDURange page can now be accessed by going to [localhost at port 50000](127.0.0.1:5000). To stop the appication, simply go to the terminal running the application and press `Ctrl + c`.

 

## New Method

This is a step by step walkthrough for instructors on how to install the new EDURange application on a new Ubuntu operating system.

 1. If you have not already, install pip3 using 
 	`sudo apt install python3-pip`

 2. If you have not already, install git using 
 	`sudo apt install git`

 3. Clone the [Github repository](https://github.com/coojac09/edurange-flask) using 
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

 9. something else