# username-and-password-database-using-prompt
This is s simple script in ansible to save the credentials of servers to a file. The default schema is hostname, username and password. You can change accroding to yoor needs
The credentails are stored to a file inside the project directory called logindb.txt
The login.txt file is located in the home directory of the user who run the script.
For exapmple if user called bob is running the script then the database location is as follow.
/home/bob/logindb.txt


Here is the sample output of the file.

[project1@control project]$ ansible-playbook -i hosts  playbook.yml
enter the hostname: server1.example.com
enter the username: bob
enter the password: redhat

PLAY RECAP *************************************************************************************************************************************************************
control.example.com        : ok=3    changed=2    unreachable=0    failed=0

[project1@control ~]$cat logindb.txt
++++++++++
 hostname:server1.example.com
 username:bob
 password:redhat
++++++++++

