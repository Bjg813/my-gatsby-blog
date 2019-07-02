---
title: Back-Up Your Wordpress Files & Database Using SSH
date: "2019-06-23"
description: Learn How to Make Secure Remote Connections From Your Command Line to Any Unsecure Network Service, Utilizing One of the Oldest & Most Reliable Protocols Around. Welcome To SSH, aka Secure Socket Shell. Start Connecting Now! (10 Min Read)
---

Using SSH, Secure Socket Shell, last week on my terminal at work was the official start of my on the job training to become database administrator. I agreed to help our web developer complete the following tasks:

1. Remotely back-up Wordpress via command line with SSH
2. Change permissions via command line with SSH
3. Manulaly update plugins
4. Update new versions of Wordpress
5. Configure cache plugin
6. Upgrade to PHP 7.1
7. Update depricated PHP scripts

These tasks need to be completed on time with the goal of freeing up space on our designated local server. 

This inspired me to do my own research over the weekend and blog about it on my free time.

If you are interested in learning more about how to use SSH in your command line to back-up Wordpress files and to change the permissions of files, then please keep reading. 

## Securely Back-Up Wordpress Files In Command Line With SSH

If you are new to Wordpress like me and you need a way to quickly back-up website files so you can make changes without worrying about losing your client's website or your job, then SSH protocol is the way to go.

First, you must make sure the web server you are connecting to is enabled either by setting it up yourself via your server admin or requesting SSH access from your hosting provider.

Second, download and setup an SSH client on your desktop. [PuTTY is an open source option](https://www.putty.org/). 

Third, login to your server via SSH using the command.

`SSH username@server-ip-address -p password` 

Fourth, your terminal will request your server password created during your setup. Note: you will not see characters of your password in the terminal, hidden for your security. You may copy and paste your password when prompted as well.

Lastly, you should on your local web server now if everythign went right. If you are not logged in, make sure you typed everything correctly or inform your host provider.

Now that you are logged into your remote web server via SSH, you can pass commands via your command line and the remote server will complete those commands for you. This is done immediately and securely, the real power of SSH.

Make sure you can view the Wordpress files located on the web server by typing `ls`. This will give you the list of directories on the server. If you see **httpdocs** in your prompt, then you are in the right place.

We want to back-up and zip the **httpdocs** directory and we will quickly do this by typing.

`zip -r httpdocs.zip httpdocs`

The first part is `zip` that is notifying the server you want to zip the following file. Next we have `-r` which stands for recurisive which is a fancy word for copy and save. Then we name the file which we named `httpdocs.zip` because that makes sense and is easy to identify. Last we have `httpdocs` which is the file we actually want to copy and zip.

This in turn created an updated copy of our **httpdocs** directory and zipped it onto our server. Now if we make any changes to our Wordpress plugins or if anything goes pear shaped, we have the newest copy of our files we can easily retrieve. 

## Make a Back-Up of Your Wordpress Database

Next we need to make a quick back-up of our websites database. We will have to do this using [phpMyAdmin](https://www.phpmyadmin.net/) gui. This can be acheived by logging into your hosting and accessing your database through their phpMyAdmin link. Usually located in preferences or admin. If you are unsure where it is, ask your hosting provider.

Once in phpMyAdmin, make sure your root directory is selected then hit **Export** located at the top right hand corner of your view port. It will open the next window and just hit **Go** at the bottom left of your view port. This will automatically download a back-up database into your Downloads directory. 

Now we are ready to safely update plugins and do whatever it is we need to do as database administrator. 

## Change File Permissions Via SSH Command Line

Encountering issues downloading [W3 Total Cache](https://wordpress.org/plugins/w3-total-cache/) where my server wouldn't let me install this plugin due to default permission accessibility. I did not know what this meant and I searched the internet for what I can do to fix this issue so I could install this caching plugin. 

> "You couldn't have screwed it up that bad yet" - Our Developer

I quickly asked our web developer and he told me I needed to change the server permissions to write instad of read. Our web developer had set the default permissions to read for security reasons.

He showed me how to do this by changing directories into the **httpdocs** then typing. 

`chmod 644 .htaccess` & `chmod 644 wp-config`

This allowed me to successfully install and configure the W3 Total Cache plugin.

Once I was done I changed the permissions back to read only and I accidentally typed **chmod 444 httpdocs** I immedately got an error and I thought I broke the Wordpress site. I notified our web developer and he laughed. He told me to tpye **chmod 755 httpdocs** and said "you couldn't have screwed it up that bad yet" which I thought was funny and made me understand permissions better and inspired me to write this blog.

Anyways, the site was returned its default permissions and was updated successfully with its new caching plugin.  

## In Conclusion

If you have followed along or just skimmed the headlines, thank you for taking the time to read my blog.

I am inspired to write every new thing I learn as a web developer so I can fully understand what I am doing and to share my knowledge with other budding web developers.

_This blog post was inspired by my acknowledgement that life is about progress and not perfection!_