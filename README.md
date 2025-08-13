Script:
#!/bin/bash for i in 
$(seq 1 100); do
username="mycompus
r$i"	useradd -m -d
/home/$username -s
/bin/bash -G wheel
$username	echo
"$username:$usernam
e" | chpasswd	chage -
M 30 $username
chmod 700 
/home/$username
done
echo "All user accounts have been created and passwords are set to expire every month."


This script automates the creation of 100 user accounts with unique usernames (mycompusr1, mycompusr2, etc.). It sets up home directories, assigns passwords matching the usernames, enforces password expiration every 30 days, and secures home directories with appropriate permissions. Finally, it notifies the administrator that the process is complete.
