## EDURange Database Guide

This is a reference guide for EDURange developers on the EDURange Database.


#### Models.py

The `models.py` file contains code that allows for the creation of the databse upon initialization of the application. Each class within the file has information about a specific table in the database.


#### Postgresql Database

The database can be accessed by using the command `sudo -u postgres psql` in the application root folder. The `\c` command followed by the name of your database will connct you to the database. The `\dt` command will show you all of the tables in the database.


###### Users Table

The `users` table, which is created by the `User` class in `models.py`, is the table that holds all user information. 
The stored information is:
- `id` - the user id
- `username`
- `email`
- `password` - the users password hash
- `created_at` - the date and time when the user account was created
- `active` - whether the user account has shown recent activity
- `is_admin` - a boolean value showing whether the user has admin privelages
- `is_instructor` - a boolean value showing whether the user has instructor privelages


###### Groups Table

The `groups` table, which is created by the `StudentGroups` class in `models.py`, is the table that stores data about student groups.
The stored information is:
- `id` - the group id
- `name` - the name chosen for the group
- `owner_id` - the user id of the instructor that created the group
- `code` - the randomly generated code that allows users to join the group upon creating their accound
- `hidden` - a boolean value that hides the group from various forms on the webpage. Solely used by the `ALL` group.
The `groups` table has one relation value. This value is the `owner_id` which is linked to the `users` table. The `owner` entry in the `StudentGroups` class in creates this relation.


###### Group Users Table

The `group_users` table, which is created by the `GroupUsers` class in `models.py`, is a relational table that links the `users` table and the `groups` table.
The table stores:
- `user_id`
- `group_id`
In the `GroupUsers` class in there are two more entries, `user` and `group`, which create the relations between the tables.


###### Scenarios Table

The `scenarios` table, which is created by the `Scenarios` class in `models.py`, is the table that stores data about scenarios.
The stored data is:
- `id` - the scenario id
- `name` - the scenario name
- `description` - the type of scenario
- `owner_id` - the user id of the instructor that created the scenario
- `created_at` - the date and time when the scenario was created
- `status` - an integer value that encodes the status of the scenario (whether the scenario is running, stopped, or errored)
The table has one relation entry, which is the `owner_id`, which links to the `users` table. In the `Scenarios` class in `models.py` there is an `owner` entry which creates the relation to the `users` table.


###### Scenario Groups Table

The `scenario_groups` table, which is created by the `ScenarioGroups` class in `models.py`, is a relational table that links the `scenarios` table and the `groups` table.
The table stores:
- `group_id`
- `scenario_id`
In the `ScenarioGroups` class there are two more entries, `group` and `scenario`, which create the relations between the tables.


###### Responses Table

The `responses` table, which is created by the `Responses` class in `models.py`, is the table that stores information about student responses to scenario questions.
The stored information is:
- `id` - the response id
- `user_id`
- `scenario_id`
- `question` - number of the question being responded to
- `student_response` - the answer submitted by the student
- `correct` - a boolean value showing whether the submitted answer was correct or not
- `response_time` - the date and time when the student submitted their answer
- `attempt` - the number of times the scenario has been attempted by the student
In the `Responses` class there are two more entries, `user` and `scenario`, which create the relations between the tables.