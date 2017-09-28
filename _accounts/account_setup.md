---
title: Account Setup
layout: page
order: 2
---



-   Generate ssh2 (openssh format) key pair on your personal computer or
    another host where you have an account. See [SSH
    Introduction](/resources/ssh_introduction "SSH Introduction").
    Use a passphrase when generating your keys, you will use this
    passphrase for your logins on the cluster.

-   Send your public key (file that ends with *.pub*) to nbcr-admin@ucsd.edu 
    Keep your private key safe and never share it.

-   Once your key is added to your new account on a cluster, you will
    receive an email confirmation with information about your account
    Use ssh to login to your account:

        ssh -l YourAccount cluster.name.here
        or
        ssh YourAccount@cluster.name.here

    If your private key is in a non-standard location you can specify Its
    location using the "-i" parameter in SSH, for example:

        ssh -i /path/to/private_key -l YourAccount cluster.name.here


-   **For users with MacOS laptops** <br>
    If you have an openssl version 7+ you
	will need to do an extra step to use your DSA type ssh key. 
    Check your openssl version with :

        openssl version

    If more than 7, do one of 

    (1) add a line to your ~/.ssh/config file (create if does not exist)

        PubkeyAcceptedKeyTypes +ssh-dss

    (2) re-create a new ssh keyin RSA format with 

        ssh-keygen -t rsa

     and email its public part.
    

<p></p>
[Back to Accounts][1]


[1]: /accounts

