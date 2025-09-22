Cronjobs are jobs that run after fix period of time like task scheduler in windows.

##### /etc/crontab
The command is list all the available conjobs.We need to see the customization cronjobs which we can use for our privilege escalation

##### cronjob file
If we see any suspious file, we can justify if this file is used for cronjobs or not to do that we can run the following command

##### ls -al
which make all the permision and time who is owner of that file(chance for root),when the file last executed or modified.

#### pspy
pspy is a github tool is used to make a list of the process is running.All cron jobs are run after a period of time.
We can confirm  that if any file/process run after fixed period of time repeatedly.

#### Resources
https://medium.com/@amaraltohami30/cron-wild-cards-privilege-escalation-linux-privilege-escalation-40f5fe084c8e
https://www.youtube.com/watch?v=BOkWLDxMaWE&list=PL-DxAN1jsRa818Ew7WI1_ngpULwDDESSI&index=4
