custom_backup
=============
Django backup application.

Creates zipped backup from your project directory and project databases dump.
Project directory is to be in DIRNAME of your Django project settings.

Backup file stored in 'backup' subdir of project with name of backup timestamp.

Backup is made by 2 ways:<br/>
  -make_backup management command<br/>
  -'/dump' url (superuser login is controled), you have to include app's urls in configuration. You will receive backup as a response.

Database drivers supported: postgres_psycopg2, mysql, sqlite3.

It is also possible to include external databeses and directories in backup, look into local app's settings.py:<br/>
APPEND_DATABASES - syntax is same as Django settings.DATABASES<br/>
APPEND_DIRS
