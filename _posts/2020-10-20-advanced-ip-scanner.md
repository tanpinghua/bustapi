---
layout: post  
title: Advanced IP Scanner
categories: tools
---

Advance IP Scanner is a IP scanning tools that can help in finding the IP Address for your connected Raspberry Pi. It is very useful especially when you are setting up the RaspberryPi in headless mode.

To download this tool, head over to its official page [here](https://www.advanced-ip-scanner.com/){:target="_blank"}. Click on the **Download** button to download the installer. 

<img src="https://docs.google.com/drawings/d/e/2PACX-1vRsIdLPprp1qnn6KhdbgEQEQPlPOatqmX5Z_GxBJVQQzunk0OCizcJ6ngwrVBdoFR6alXUJ4zhkvlTy/pub?w=938&amp;h=676">

Under the main application page, you can configure the range of IP address to scan and trigger the start of the scanning. 

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQEUpR5ep00YRKap56zY5vOmSi_EAgPLJtavqSVf1viA1Tw2-kSO33sejEoA8kEbddc2_U9bHJGiLmJ/pub?w=953&amp;h=658">

Basically the system will scan through the range of IP address and display the list of available device found in the range. I found out that in order to get a better result, it is recommended to turn on the High-accuracy scanning in the options. Navigate to **Settings > Options > Performance** and click on the "High-accuracy scanning (lower speed) checkbox and click OK. 

<img src="https://docs.google.com/drawings/d/e/2PACX-1vTAx_y7XC9pxjX6ekzx9b9Y0D_NWqnN2Rvg8LXkzM9DN6JsAfemCv6Vctw7jwi0DHMFL3Fxa--LBkVb/pub?w=955&amp;h=644">

After clicking the Scan button, my system took roughly 2 minutes to complete the scan, I have around 30 devices connected to my router. From the result, you can get the Name, IP Address, Manufacturer and MAC address of all connected device on the same network, and from there you can find the IP Address for the connected Raspberry Pi. Do make sure that the hostname for the RaspberryPi is as default "raspberrypi" or you should see your custom hostname under the list. 

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQJBSnLD2nX9XTrOSxbbng0Hr2IEtPZDhqfyj7MFa_pIKYjMtn2NsgAX4jwmBockMDXHDfUjcEOxG63/pub?w=959&amp;h=615">
