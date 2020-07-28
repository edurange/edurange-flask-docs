## Instructor Page Guide

This is a reference guide of the pages for instructor use.


This guide is divided into sections by what pages can be found using each type of view available to an EDURange instructor using this webpage. To switch the current view, click the username in upper right hand corner of the page and select the desired view using the drop down menu.

![View Switcher](/assets/inst/page_guide/viewSwitcher.png)



---


#### Admin View

The `Admin View` gives the instructor access to the `Admin Dashboard` and `Scenarios` table.


On the `Admin Dashboard` an instructor can find various tables and forms. The tables include the `All Instructors` table, the `Manage Students` table, and the `All Groups` table. The forms include the `Create Student Group` form, the `Manage Students` form, and the `Manage Instructors` form.

![Admin Dashboard](/assets/inst/page_guide/adminDash.png)



###### Admin Tables


The `All Instructors` table allows an instructor to see information about any user with instructor privelages. The table will display the users id, username, and email.

![All Instructors](/assets/inst/page_guide/admin/allInstructors.png)



The `Manage Students` table shows an instructor all of the students that are registered. The table displays each students id, username, and email. The table also allows instructors to add and remove students from groups using the group drop down menu, student selection buttons, and submit buttons.

![Manage Students](/assets/inst/page_guide/admin/manageStudents.png)



The `All Groups` table, is a set of tables for each student group. The table for each group displays the groups name and registration code, as well as information about the students in the group such as id, username, and email.

![All Groups](/assets/inst/page_guide/admin/allGroups.png)



###### Admin Forms


The `Create Student Group` form allows an instructor to create a new student group with any name. It also allows for the bulk generation of student accounts for the group with a maximum of 40 possible accounts that can be handed out to students in a class.

![Create Student Group](/assets/inst/page_guide/admin/groupMaker.png)



The `Manage Students` form allows an instructor to delete students from the database. To do so a username must be entered. This process cannot be undone. [currently the form does not work]

![Manage Students](/assets/inst/page_guide/admin/studentManager.png)



The `Manage Instructors` form lets an instructor give a user instructor privelages. The form also lets an instructor take these privelages away. **Note** that the instructor privelages granted by this form are **not** the same that the admin will have. It will only allow a user to have their on instructor view. This **will** give them the ability to create student groups and scenarios on the admininstrators machine. [This is likely best reserved for TAs]

![Manage Instructors](/assets/inst/page_guide/admin/instructorManager.png)



###### Scenarios Table


The `Scenarios` table lets an instructor see all of the scenarios that they have created for their groups. The table displays each scenarios name, type, owner, date of creation and status. The table also allows the instructor to start, stop, and destroy each scenario. The listed name of each scenario doubles as a button to send the instructor to a page with more information about the selected scenario. At the top of the page is a button that allows the instructor to create a new scenario.

![Scenarios table](/assets/inst/page_guide/scenarios.png)



The scenario creation page is accessible by pressing the `New Scenario` button at the top of the `Scenarios` table. This page is a form that allows an instructor to create anew scenario with a unique name, a selected student group, and a selected scenario type.

![New Scenario](/assets/inst/page_guide/scenarios/scenarioMaker.png)



The scenario information page is accessible by pressing the listed name of a scenario on the `Scenarios` table. The page displays various details about the selected scenario.

![Scenario Info](/assets/inst/page_guide/scenarios/scenarioInfo.png)



---


#### Instructor View


The `Instructor View` allows an instructor access to the `Instructor Dashboard` and the `Scenarios` table which is identical to the table visible to the admin.


On the `Instructor Dashboard` an instructor is given access to the `Owned Groups` and `Student Responses` tables, as well as a `Create Student Group` form.

![Instructor Dashboard](/assets/inst/page_guide/instructorDash.png)



###### Instructor Tables


The `Owned Groups` table lets an instructor see the groups that they own. If the instructor is also the Admin, then the *`ALL`* group will also be visible. The table will display the groups id, name, and registration code.

![Owned Groups](/assets/inst/page_guide/instructor/ownedGroups.png)



The `Student Responses` table will let the instructor see the submitted by their students in each of their groups. [This table is not yet implimented]

![Student Responses](/assets/inst/page_guide/instructor/studentResponses.png)



###### Instructor Forms


The `Create Student Group` form allows an instructor to create a new student group with any name. THis form however does not allow for bulk student account generation.

![Create Student Group](/assets/inst/page_guide/instructor/groupMaker.png)



---


#### Student View


The `Student View` allows an instructor to view their own student `Dashboard`.

On the student `Dashboard` a user can find the `User Info` table, the `Member of Groups` table, and the student `Scenarios` table.

![Student Dashboard](/assets/inst/page_guide/studentDash.png)



###### Student Tables


The `User Info` table displays information about the current user, including the user id, username, and email.

![User Info](/assets/inst/page_guide/student/userInfo.png)



The `Member of Groups` table displays information about the groups that the current user is a member of. The table displays the each group id, and group name. [It will likely be difficult for there to be any information on theis table for the application admin]

![Member of Groups](/assets/inst/page_guide/student/groups.png)



The student `Scenarios` table allows a user to see what scenarios they are a part of. The table will display the name and type of the scenario, as well as the related group and instructor. [It will likely be difficult for there to be any information on theis table for the application admin]

![Student Scenarios](/assets/inst/page_guide/student/scenarios.png)


