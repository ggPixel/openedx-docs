# openedx-docs
Documentation for installing, configuring and managing the Open Edx platform

## Restart Edx Services

#### LMS/CMS
`sudo /edx/bin/supervisorctl restart edxapp:`

#### Workers
`sudo /edx/bin/supervisorctl restart edxapp_worker:`

## Delete a single course

1. Navigate to the edx-platform directory `cd /edx/app/edxapp/edx-platform`
2. To get the full list of course IDs, run this command ` sudo -u www-data /edx/bin/python.edxapp /edx/bin/manage.edxapp lms dump_course_ids --settings aws`
3. Replace the <course ID> in the following command with the Course ID you would like to delete and run the command `sudo -u www-data /edx/bin/python.edxapp /edx/bin/manage.edxapp cms delete_course <COURSE_ID> --settings aws`
  4. erify the course has been deleted by running the command in step 2
