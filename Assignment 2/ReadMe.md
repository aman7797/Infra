# Configure Linux Postfix Mail Server

To make the server a public mail server,we have to change the IP with the public IP. We can do that by changing the hosts file.
    
    vi /etc/hosts

![PostFix Installation](\img\HostFile.PNG)

It will open file as shown in the image you can change it by pressing `Esc+i`

Add the following line  
115.110.197.158 server.aman.local server2


## What is Postfix? 
It is Wietse Venema's mail server that started life at IBM research as an alternative to the widely-used Sendmail program. Now at Google, Wietse continues to support Postfix.

## Postfix Installation

Postfix can be installed by the following command and please remove the sendmail if already installed.

    yum remove sendmail
    yum install postfix

![PostFix Installation](\img\InstallPostfix.PNG)


10.0.2.54/24
10.0.2.255