Netcash Pay Now - CS-Cart 4 Payment Gateway Module
===============================================

Revision 2.0.0

Introduction
------------

Netcash South Africa's Pay Now third party gateway integration for CS-Cart 4. This module gives you to access the Netcash Pay Now gateway which in turns lets you process online shopping cart transactions using CS-Cart 4. VISA and MasterCard are supported.

Download and Database Table Installation Instructions
------------------------------------------------

1. Download the files from Github:
* https://github.com/Netcash-ZA/PayNow-CSCart4/archive/master.zip

Copy the files into your CS-Cart /app /design folders.

2. Inside the file downloaded above is a file called 'install.paynow.sql'.

This file has to be executed against your CS-Cart installation database.

If you are using a web hosting control panel such as cPanel or Plesk, it will be possible to run this file by using PHPMyAdmin which is built into those panels.

If your database is not hosted you can use an application such as SQLYog to install the database file.

A 30 day trial of SQLYog can be downloaded here:
https://www.webyog.com/product/downloads

Once SQLYog is running, connect to your database and run the file.


Configuration
-------------

Prerequisites:

You will need:
* Netcash login credentials
* Netcash Pay Now Service key
* CS-Cart admin login credentials

A. Netcash Pay Now Gateway Server Configuration Steps:

1. Log into your Netcash account
	https://merchant.netcash.co.za/SiteLogin.aspx
2. Type in your Netcash Username, Password, and PIN
2. Click on Account Profile
3. Click on NetConnector
4. Click on Pay Now
5. Click "Active:"
6. Type in your Email address
7. Click "Allow credit card payments:"

8. The Accept, Decline, Notify and Redirect URLs should all be:
	http://www.YOUR_DOMAIN.co.za/app/payments/paynow/paynow_callback.php

9. It is highly recommended that you "Make test mode active:" while you are still testing your site.

B. CS-Cart Steps:

1. Log into CS-Cart as administrator (http://cscart_installation/admin.php)
2. Navigate to Administration / Payment Methods
3. Click the "+" to add a new payment method
4. Choose Netcash Pay Now from the list and then click save.
5. Once you have added the payment method, click on the cog wheel to configure the payment method
6. For template, choose "cc_outside.tpl"
7. Click the 'Configure' tab
8. Enter your Netcash Pay Now service key
9. In the order status conversion map, match Completed to Processed and match Failed to Failed.
10. Click 'Save'

You are now ready to transact. Remember to turn of "Make test mode active:" when you are ready to go live.

Issues & Feature Requests
-------------------------

We welcome your feedback.

Please contact Netcash South Africa with any questions or issues.
