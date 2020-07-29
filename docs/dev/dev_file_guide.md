## EDURange File System Guide

This is a reference guide for developers on the EDURange application file system.


#### Python Files

Python files make up most of the basis for the front end of the application. Most are found within the `edurange-refactored` directory.


###### user/views

The `user/views.py` file contains the inner workings of the main dashboard pages on the EDURange webpage. For each webpage there is  a blueprint route and a related function which contains the functions and queries that supply the information for the page.


###### models

The `models.py` file contains information about the applications database. The file has a class for each table in the database. If changes are to be made to the database, then they can be made in this file so that when the database is re-created the changes will be implimented automatically.


###### utils

The `utils.py` file contains various functions that are used in many other files in the application. It also contains functions for single files that would clutter those files.


###### autoapp

The `autoapp.py` file is one of the most important files in the application. This file is found in the applications root directory and it details how to initialize the application.


###### settings

The `settings.py` file contains information important to the initialization of the application. This file determines whether the application is running in a development environment or a production environment. It is also where the applications mail server is set.


###### scenario_utils

The `scenario_utils.py` file contains utility functions used in the handling of scenarios by the application. Many of the functions write terraform files for each new instance of a scenario. Others support the front end scenario creation process.


---


#### HTML Files

The HTML files of the application are found in the `templates` directory. They determine how the application webpage is displayed and interacted with the user.

Utility HTML files can be found with no subdirectory. These files are error pages and formatting pages that are used by other files in the subdirectories.


###### dashboard

The files that can be found in the `dashboard` directory are templates for all of the pages which are password protected. These files act as dashboards for the users, displaying important information and providing important functionality to the website.


###### public

The files in the `public` directory are templates for the pages that can be accessed without creating an account on the application. These pages include the websites home page as well as the account registration page.


###### utils

The `utils` directory contains files that allow a user to reset their password via email.


---


#### Scenario Files

Files for the EDURange ecenarios can be found in two directories, `data/tmp/` and `scenarios/prod/`.

Files in the `scenarios/prod/` directories are the basis for each type of scenario. If a new type of scenario is introduced, its files should be places within these directories.

Files in the `data/tmp` directories are files for instances of each type of scenario. They will have the name that the instance of the scenario was given when it was created. In these directories will be `.tfstate` files, which will contain information about the current state of the scenario and the students who are a part of it.

---


#### Requirements

The `requirements` directory contains two text files. These files are used in the application installation process to automatically pip install pachages that the application needs to run. 

The `dev.txt` file allows the installation of tools useful for development of the application. The `prod.txt` file contains installation instructions for tools needed to run a production variant of the appication.

