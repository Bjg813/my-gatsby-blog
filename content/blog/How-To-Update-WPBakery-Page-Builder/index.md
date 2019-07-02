---
title: How To Update WPBakery Page Builder From Your Dashboard?
date: "2019-07-01"
description: Learn the Quickest & Easiest Way to Update WPBakery Page Builder From Your Wordpress Admin. Start Updating Now! (5 Min Read)
---

Updating WPBakery Page Builder seems harder than it really is. In this short blog you will learn the fastest and easiest way to update WPBkery Page Builder from your Wordpress Dashboard. 

**Note:** Before you do anything, update your Wordpress files and database. If you don't know how to do this, follow my blog post on [backing-up your Wordpress files and database using SSH](/Back-Up-Wordpress-Files-&-Database-Using-SSH/). 

## 1. Find Newest Version of WPBakery

Only way I have found the newest version of WPBakery Page Builder, was by downloading a new theme. Newest WPBakery version is packaged in the theme directory. 

Once in the theme directory, look in **wp-content/plugins/js_composer** and unpack the **js_composer.zip** file from the direcotry. Move this file to your desktop for future use.

## 2. Remove Outdated WPBakery Plugin

Go to **plugins** in your Wordpress dasboard and find your outdated WPBakery plugin. Do the following simple two steps:

1. Deactivae WPBakery plugin
2. Delete WPBakery plugin

You are halfway done! Keep Truckin'

## 3. Ensure You Can Upload Large Files

Contact your hosting services and request to change the default file size upload allowances to at least 25MB. 

If you have access to your own hosting then do it there.

I read you can also do this from your .httpaccess file, however I do not recommend changing your .httpaccess file ever unless it is absolutely necessary. 

## 4. Install New WPBakery Version

Go to **plugins** again in your Wordpress dashboard. Once you are in the plugin dashboard, cLick **add new** at the top. 

Once you are in the plugin locator, click the **Install Plugin** button. This will prompt a choose file to upload window. Click the choose file button and find your **js_composer.zip** file from your dashboard. 

Click the **js_composer.zip** file and upload this file. Wodpress will notify you it is loading your file and will take between 10-30 seconds depending on your internet speed. 

Once WPBakery is fully loaded, it will prompt you to activate the plugin. Do so by clicking the activate button.

Thats it! 

Your WPBakery Page Builder plugin has been successfully installed with the newest version and has been updated

## In Conclusion

It is really easy to update and install WPBakery Page Builder. 

Update your plugins as often as you can. Remember to always update your files and database before you update any plugins. 

Not only will this give you a reliable back-up in case something goes pear-shaped, it also gives you piece of mind and teaches you how to be a professional. 

Good luck and Dev on!

_This blog was inspired by only having the WPBakery Page Builder zip file on hand, whilst alone in the office on a Friday afternoon_





