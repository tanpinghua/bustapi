---
layout: post  
title: Raspberrypi Headless Setup  
categories: how-to
---

This article explains the step by step in setting up a headless Raspberrypi running on Raspberry Pi OS without connecting it to Monitor and Keyboard.

A standard method of setting up a Raspberrypi, involves writing the image file onto the SDCard, insert the SDCard into a Raspberrypi, and normally it will require a monitor and keyboard for the first boot to configure the WiFi, SSH, VNC, and etc. However we noticed that in a lot of scenario, we are not able to connect this RaspberryPi to a Monitor and a Keyboard. In this guide, the steps involved here will get you onto your Raspberrypi without the need for a Monitor or Keyboard.

### Write image file onto SDCard

First, to write the Raspberry Pi OS, you can refer to [this]({% post_url 2020-10-18-write-image-file-to-sdcard %}){:target="_blank"} guide for more details. After you have the SDCard written, before inserting them into your Raspberry Pi, insert them into your PC as we will need to add some files onto it. If you have just completed the Raspberry Pi Imager, you might need to remove and re-insert the SDCard as the Raspberry Pi Imager will automatically unmount your SDCard from your PC.

### Add in "ssh" and "wpa_supplicant.conf" file to boot drive

After inserting the SDCard to your PC, you should see a drive called **boot** in your My Computer windows. Sometimes your computer might show a message saying that "you'll need to format the drive to continue". You can ignore the message as it is due to the ext4 drive format that is not supported by Windows. 

<img src="https://docs.google.com/drawings/d/e/2PACX-1vT8Ps9XrejP3eaSNwkRJtHIiLVlUAAIFas6P7HwqolSN0rQC6_ymys5gimbUh_soIQc2msPy6fEBXZa/pub?w=960&amp;h=649">

Under this boot drive, you are required to add 2 files, the first one is "ssh" file. Take note that you will need to create an empty "ssh" file that does not has any extension. Before you proceed to next step, in order to avoid the confusion for the file extension, it is recommended to first show the extension for your File Explorer. At your Windows File Explorer, navigate to **View > Options > View** and uncheck the "Hide extensions for known file types".

<img src="https://docs.google.com/drawings/d/e/2PACX-1vSpW2QSNeUBCCOdYqC8jWMRQycIRu8q461NgreE59E1TjFtQwbfcG4usSScze1AEZz66M4S9QidsQyo/pub?w=866&amp;h=879">

Now, navigate to the **boot** drive and you should see all the extension the files under this drive. Right click on the empty space and create a new Text Document.

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQjD-fR037WIqEFvZLKz31Q5heCUhJ57n4jNbF-WMBpfDrOUus4tk3M6ToYSKao7BKcH92J1xuf2iGQ/pub?w=916&amp;h=715">

Rename the "New Text Document.txt" to "ssh" without any extension. It should warn you about the changes of the extension, click Yes to apply. Now you should have a "ssh" file in your **boot** drive.

<img src="https://docs.google.com/drawings/d/e/2PACX-1vSyit-ZfBRrWScrQIlIB4PxBn3xl5HwxwBqCh5exPJEtcZTLX2ip-B2fqX8j7fWdt89qlK7Vb6VjruP/pub?w=944&amp;h=1105">

Next you will need to create a file called "wpa_supplicant.conf" under the same **boot** drive. Repeat the same steps as for the "ssh" file but this time, the filename is "wpa_supplicant.conf". Do take note that the file name has to be exactly "wpa_supplicant.conf".

<img src="https://docs.google.com/drawings/d/e/2PACX-1vRE5LHmb5K_hO8k5xwUEnUy3hsRG9Qiz1PgWE7ca2Cvn8AIspjnhRE_8iflko1LIDjeE8E55l2_5H3f/pub?w=958&amp;h=494">

### Edit wpa_supplicant.conf according to your WiFi setup

Next edit this file by using Notepad++ or any text editor that is available for you.

<img src="https://docs.google.com/drawings/d/e/2PACX-1vTgmRY23d1E_sCSSbEjyloZ7EjDoXlgalyrww2BbmBjj7zwfZae95pyLwUwMB3EGqx-4hJdTxWp2GJa/pub?w=958&amp;h=612">

Replace the country code, ssid and psk according to your country and WiF setup. You can refer for more information about wpa_supplicant.conf [here]({% post_url 2020-10-20-wpa-supplicant-reference %}){:target="_blank"}. After that, save the file, and eject the SDCard from your PC. The SDCard are now ready for the first boot up.

### First boot up

Insert the SDCard into your Raspberry Pi, take note that we are using WiFi communication for the connection through SSH, so you will need to use the Raspberry Pi that has built-in WiFi module. Connect the power connector and it should boot up accordingly. Also be sure that the RaspberryPi is within the coverage of the WiFi configured onto wpa_supplicant.conf file in the previous steps. 

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQuabd-FJcBRaIX1-7At3weWDDbkIklNHnnzbDQCYMMNWc0xXHIFWt5636YYDSACNjU0pN_6QlWV2Ie/pub?w=817&amp;h=696">

For the first bootup it should take some time for the initial configuration, the expansion of partition and etc. After which it should be automatically connected to the WiFi according to your wpa_supplicant.conf file. In order to get the IP Address of the RaspberryPi, there are several ways. In this guide I am using Advance IP Scanner to scan through all the connected device in my local network, and eventually find the IP Address of the RaspberryPi.

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQJBSnLD2nX9XTrOSxbbng0Hr2IEtPZDhqfyj7MFa_pIKYjMtn2NsgAX4jwmBockMDXHDfUjcEOxG63/pub?w=959&amp;h=615">

Aside from using this method, you can also check the connected device via your Router page, or you can use zeroconf method, or there are actually tons of way to get the IP address of your connected RaspberryPi.

### SSH to the Raspberry Pi

After getting the IP Address, you can now access the device through SSH. 

