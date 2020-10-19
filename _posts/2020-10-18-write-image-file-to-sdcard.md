---
layout: post
title: Write Image File onto SDcard
categories: how-to
---

This article share the step by step on how to write a Raspberry Pi image onto SDcard.

## Using Raspberry Pi Imager

The simplest way to write image file onto SDcard is by using official Raspberry Pi Imager from Raspberry Pi. You can get the Raspberry Pi Imager from the official Raspberry Pi download page [here](https://www.raspberrypi.org/downloads/){:target="_blank"}.

Choose the download according to the operating system of the computer that you will use to write the image file. 
<img src="https://docs.google.com/drawings/d/e/2PACX-1vTXKTixmfXPOVivINy1wMpD3B_ohDypFGnxU7-BmXCTf13FX3CrU0LFZfn0xoMx7LIjOpUyrbk5v7RX/pub?w=951&amp;h=714">
<!--more-->
For Windows version, you will need to install it onto your PC. After completing the installation, run Raspberry Pi Imager from your PC, and this will be the main windows. 

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQ00Qmn4cTI4CHaBp7YYJk2_QF9XakA2eRxDPqGApEHEBWu4CA6ttsd0SbLwDx2zMBpAqAM7rHoPh5O/pub?w=813&amp;h=622">

For the Operating System, you will have a few options to choose from:
* Raspberry Pi OS (32-bit) - recommended
* Raspberry Pi OS (other)
* LibreELEC
* Ubuntu
* RetroPie
* TLXOS
* Misc Utility Images
* Erase
* Use Custom - this option allows you to specify the image file from your system

<img src="https://docs.google.com/drawings/d/e/2PACX-1vSpzK719EBfUlfvlUawP_jiVB7jeq7nOQLt0c4yeqCkdjnhjFyvcrFHYin5NyHFtjwBmKLeEldWQi4M/pub?w=926&amp;h=622">

Next step is to choose the SDCard to write to. Ensure that the SDCard you intend to write to is inserted into your PC either using USB SDCard reader or direct SDCard slot. If it is inserted correctly, it should be shown on the available SDCard page. To avoid writing to the wrong device, please remove the unused SDCard or USB drive.  

<img src="https://docs.google.com/drawings/d/e/2PACX-1vRAYsNH6JYCc8m_QpppZQzBDOlvebQ_Fkt8BCLy0aR1E3sVlGCqjrcgY1siXYMwQtjeUFCpc-2X1Vsr/pub?w=957&amp;h=647">

The last step is to click on the click on the WRITE button. Take note that it will also ask for confirmation after you've click the WRITE button.  

<img src="https://docs.google.com/drawings/d/e/2PACX-1vScxmgKyvLEIQinanXGmONGesiP2BWKTGdxqNcz1ipf98nbT-8xm9q_8YGD4ZZKMBat9Z42KiCXqvZt/pub?w=951&amp;h=636">

The write process should start after that. In my case it tooks around 25 minutes to complete, but it depends on the internet speed and the SDCard write speed. The full image file will be automatically downloaded from the internet before the write process begin. 

<img src="https://docs.google.com/drawings/d/e/2PACX-1vTq2UWrHMdm_utB0cty3EI9Ukep4FJQfaMdmEmPQEgbU3vTQt36HjcFflKSR5rx-Tl7_YtJh4PE0Nqb/pub?w=961&amp;h=641">

After it is complete, you can now remove the SDCard from your system and insert it to a Raspberry Pi. 

<img src="https://docs.google.com/drawings/d/e/2PACX-1vS8WzOql-ctTjyOGBedP9UEs7Kc2mgV7FvBXvAkG3CnHQTd_FY0Z3F3PWbKKKbiC_ve03vjhFTWfWzs/pub?w=959&amp;h=645">

