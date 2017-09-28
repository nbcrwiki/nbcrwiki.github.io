---
title:  SSH Introduction
layout: page
order: 3
---

#### Generate ssh key pair

1.  **For Linux, MacOS, Windows cygwin:**

        ssh-keygen -t dsa
        or
        ssh-keygen -t rsa

        
    You will see the output similar to 

        Generating public/private dsa key pair.
        Enter file in which to save the key (/home/tester/.ssh/id_dsa): 
        Enter passphrase (empty for no passphrase):  USE STRONG PASSWORD
        
        Enter same passphrase again: USE STRONG PASSWORD
        Your identification has been saved in /home/tester/.ssh/id_dsa.
        Your public key has been saved in /home/tester/.ssh/id_dsa.pub.
        The key fingerprint is:
        fa:7a:29:2a:4a:a7:ef:13:45:e9:35:10:a4:32:ba:16

    **Note:** do not use empty passwords as this is insecure, use a strong password.

    **Note**: You can then email your "id_dsa.pub" file. Keep the
    "id_dsa" file safe and never share it.

   **NOTE: For users with MacOS laptops** <br>
    If you have an openssl version 7+ you will need to do an extra step to use your DSA type ssh key. 
    Check your openssl version with :

        openssl version

    If more than 7, do one of 

    (1) add a line to your ~/.ssh/config file (create if does not exist)

        PubkeyAcceptedKeyTypes +ssh-dss

    (2) re-create a new ssh key in RSA format with 

        ssh-keygen -t rsa


2.  **For windows PuTTY**

    The PuTTY Key Generator, known as
    [PuTTYgen](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html "http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html")
    can be used to generate a key pair. To generate the key pair:

    -   Run the PuTTYgen.
    -   Select the option towards the bottom that says "SSH-2 DSA".
    -   Click "Generate".
    -   Copy the contents of the larger textbox where it says "Key" and
        save it using Notepad instead of Wordpad. Then send this file to
        the administrator.
    -   Enter your passphrase twice.
    -   Then "Save public key" and "Save private key". This will save
        the key pair to your computer.
    -   When saving your private key, make sure that it is in the ".ppk"
        format.
    -   To authenticate you will need PuTTY, also available at the link
        above.

    <p></p>
    If you have already generated a key, say from a different machine,
    and you want to reuse it, you may just use PuTTYGen to load the
    private key, and then use the "Save Private Key" to convert it into
    a PPK format (PuTTY format).

#### Login using ssh key pair

1.  **For Linux, MacOS, Windows cygwin:**

        ssh -l username host.name.here

2.  **For windows PuTTY: run PuTTY**

    -   Specify the hostname.
    -   In the menu to the left, under the section SSH, select "Auth".
    -   Click "Browse" to load your private key file.
    -   Now click "Open". It should now prompt you for a username and
        password. The password being the one you entered earlier when
        generating the keypair.

<p></p>
[Back to Accounts][1]


[1]: /accounts

