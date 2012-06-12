moodle-block_people
===================
Moodle block which displays all teachers of a course with contact quicklinks, as well as a quicklink to the participants list


Requirements
============
This plugin requires Moodle 2.1+


Changes
=======
2012-06-01 - Initial version


Installation
============
Install the plugin like any other plugin to folder
/blocks/people

See http://docs.moodle.org/22/en/Installing_plugins for details on installing Moodle plugins


Usage
=====
The block_people plugin displays a list of the course's teachers grouped by roles. The block shows the teacher's avatar, a quicklink to his/her profile and a quicklink to send him/her a message with the moodle message system. Furthermore, there is a quicklink to the participants list of the course.


Settings
========
block_people has neither a settings page nor settings in config.php. Nevertheless, there are some Moodle settings it responds to:

1. List of teachers
-------------------
block_people gets the list of teachers from $CFG->coursecontact. With this Moodle core setting, you can define which roles are displayed in block_people's list of teachers.

2. Quicklist for teachers
-------------------------
block_people only shows a quicklink to the teacher's profile if the user has the capability moodle/user:viewdetails
See http://docs.moodle.org/22/en/Capabilities/moodle/user:viewdetails for details on this capability

block_people only shows a quicklink to the message system if the user has the capability moodle/site:sendmessage and if the Moodle message system is turnes on ($CFG->messaging)
See http://docs.moodle.org/22/en/Capabilities/moodle/site:sendmessage for details on this capability and http://docs.moodle.org/22/en/Messaging for details on the messaging system

3. Participants List
--------------------
block_people only shows the link to the participants list if the user has the capability moodle/course:viewparticipants.
See http://docs.moodle.org/22/en/Capabilities/moodle/course:viewparticipants for details on this capability

4. Roles sort order
-------------------
block_people shows teacher role groups in the order defined in /admin/roles/manage.php. Please visit this settings page if you want to modify the sort order


Further information
===================
Report a bug or suggest an improvement: https://github.com/abias/moodle-block_people/issues
