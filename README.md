google-cloud-sshKeys
====================

google cloud ssh-key issues

Agent admitted failure to sign using the key.
Permission denied (publickey).

if you got the above error, it can happen with the two options:
1 - you used gcutil ssh name
2 - you tried to ssh to the server

check if you have the following keys under ~/.ssh/ :
google_compute_engine.pub
google_compute_engine

the .pub is the public key and should be overwrite.

please move it to /tmp and try to access the servers again (preferred with ssh).
you will be asking to enter password for the passphrase:

Enter passphrase for key '/home/name/.ssh/google_compute_engine':

enter your password and thats all, now you will be able to login.

