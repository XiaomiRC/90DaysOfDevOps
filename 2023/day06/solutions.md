1. Create a simple file and do ls -ltr to see the details of the files refer to Notes
Each of the three permissions are assigned to three defined categories of users. The categories are:

 owner   —   The owner of the file or  application.
"chown" is used to change the ownership permission of a file or directory.

 group   —   The group that owns the file or application.
"chgrp" is used to change the group permission of a file or directory.

 others  —   All users with access to the system. (outised the users are in a group)
"chmod" is used to change the other users permissions of a file or directory.

As a task, change the user permissions of the file and note the changes after ls -ltr

2. Write an article about File Permissions based on your understanding from the notes.

3. Read about ACL and try out the commands getfacl and setfacl
   **Solution**
  321  mkdir ACL
  322  cd ACL
  323  nano TEST
  324  getfacl TEST 
  325  cat /etc/passwd
  326  clear
  327  getfacl TEST 
  328  useradd sam
  329  sudo useradd sam
  330  cat /etc/passwd
  331  sudo userdel sam
  332  sudo adduser sam
  333  cat /etc/passwd
  334  clear
  335  ls -al
  336  getfacl TEST 
  337  chmod 660 TEST 
  338  ls -al
  339  clear
  340  getfacl TEST 
  341  setfacl --help
  342  setfacl -m u:sam:r TEST 
  343  getfacl TEST 
  344  ls -al
  345  getfacl TEST
  346  setfacl -x u:sam TEST
  347  setfacl -k TEST
  348  setfacl -m u:sam:rw TES
