1. You have to do the same using Shell Script i.e using either Loops or command with start day and end day variables using arguments -
So Write a bash script createDirectories.sh that when the script is executed with three given arguments (one is directory name and second is start number of directories and third is the end number of directories ) it creates specified number of directories with a dynamic directory name.

Example 1: When the script is executed as

./createDirectories.sh day 1 90

then it creates 90 directories as day1 day2 day3 .... day90

Example 2: When the script is executed as

./createDirectories.sh Movie 20 50 then it creates 50 directories as Movie20 Movie21 Movie23 ...Movie50

**MY Solution:**
```bash
vim createDirectories.sh
```
```bash
#!/bin/bash
echo "This script is to create multiple directories in a go"
echo "Example 1: When the script is executed as"
echo "./createDirectories.sh day 1 90"
echo "then it creates 90 directories as day1 day2 day3 .... day90"
echo "Input 3 parameters in the following order: one is directory name and second is start number of directories and third is the  
end number of directories"
read name first last
for ((i=$first; i<=$last; i++))
do
        mkdir $name$i
done
```
2. Create a Script to backup all your work done till now.
**MySolution:**
```bash
#!/bin/bash
source=/home/ubuntu
target=/home/ubuntu/backups

echo “backup started”

# compresses everything in my-backups from the source location to target location
tar -cvf $target/my-backups.tar.gz $source

echo “backup completed”
```
3. Read About Cron and Crontab, to automate the backup Script
Cron is the system's main scheduler for running jobs or tasks unattended. A command called crontab allows the user to submit, edit or delete entries to cron. A crontab file is a user file that holds the scheduling information.
**My Solution:**
```bash
vim test.sh
```
```bash
#!/bin/bash
source=/home/test
target=/home/test/backups
filename=$(date +'%d-%m-%Y-%H:%M:%S').tar.gz
echo “backup started for $filename”

#compresses everything in my-backups from the source location to target location

tar -cvf $target/$filename.tar.gz $source

echo “backup completed”
```
```bash
Run a cron job:
crontab -e

* * * * * /bin/bash /home/test/test
```
4. Read about User Management and Let me know on Linkedin if you're ready for Day 6.
A user is an entity, in a Linux operating system, that can manipulate files and perform several other operations. Each user is assigned an ID that is unique for each user in the operating system. In this post, we will learn about users and commands which are used to get information about the users. After installation of the operating system, the ID 0 is assigned to the root user and the IDs 1 to 999 (both inclusive) are assigned to the system users and hence the ids for local user begins from 1000 onwards.

5. Create 2 users and just display their Usernames
**My Solution:**
```bash
useradd Ana
useradd Amanda
awk -F':' '{ print $1}' /etc/passwd
```
