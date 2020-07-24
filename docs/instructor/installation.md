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

 4. The EDURange page can now be accessed by going to [localhost at port 50000](127.0.0.1:5000). To stop the appication, simply go to the terminal running the application and press `Ctrl` + `c`.

 