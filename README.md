# Automating-Database-Backup-with-Jenkins
The task involved creating a Jenkins job to automate the database backup process. The following steps were followed to accomplish this:

1. Generated a private key on the database server and copied it to the backup server using "ssh-copy-id". This ensured that Jenkins could SSH into the server without requiring a password.

2. Installed the SSH plugin on Jenkins to enable running commands on the database server. Used SCP to copy the backup file to the backup server.

3. Created a Jenkins job named "database-backup".

4. Configured the job to take a database dump of the "kodekloud db01" database present on the Database server in the Stratos Datacenter. The database user is "kodekloud roy" and the password is "asdfadsd".

5. The dump was named in the "db_(date +8F).sql" format, where "date +8F" represents the current date.

6. Copied the "db_(date +8F).sql" dump file to the Backup Server under the location "/home/clint/db_backups".

7. Scheduled the job to run automatically every 10 minutes using the schedule format "*/10 * * * *".

By automating the database backup process with Jenkins, the task ensures regular and efficient backups of the "kodekloud db01" database. This reduces the risk of data loss and allows for easy restoration if needed.

Attached is the screenshot of the completed task.

<img width="1509" alt="Screenshot 2023-09-10 at 09 07 29" src="https://github.com/boltpius/Automating-Database-Backup-with-Jenkins/assets/127052041/7733c498-de2a-4e36-8b1d-b1d039a62fa9">

<img width="1509" alt="Screenshot 2023-09-10 at 09 08 44" src="https://github.com/boltpius/Automating-Database-Backup-with-Jenkins/assets/127052041/f4c6f725-e5cc-4fab-81df-196009843ff4">

<img width="1509" alt="Screenshot 2023-09-10 at 09 15 52" src="https://github.com/boltpius/Automating-Database-Backup-with-Jenkins/assets/127052041/4a7c15c5-0e17-44e7-b7e7-baad1d0aeaa1">

<img width="1509" alt="Screenshot 2023-09-10 at 09 22 00" src="https://github.com/boltpius/Automating-Database-Backup-with-Jenkins/assets/127052041/808baa6b-b7a1-4941-a0f8-0387807a3c3f">

<img width="1509" alt="Screenshot 2023-09-10 at 09 24 49" src="https://github.com/boltpius/Automating-Database-Backup-with-Jenkins/assets/127052041/4f7a21c0-5525-43c7-b2bc-de1c0f533c4b">

<img width="1509" alt="Screenshot 2023-09-10 at 09 26 48" src="https://github.com/boltpius/Automating-Database-Backup-with-Jenkins/assets/127052041/1fda979a-cffa-4a78-8499-56f27d13a09a">

<img width="1509" alt="Screenshot 2023-09-10 at 09 28 00" src="https://github.com/boltpius/Automating-Database-Backup-with-Jenkins/assets/127052041/670e0da8-e8b0-4177-a452-fd83f37864a8">







