---
layout: post  
title: WPA Supplicant Reference
categories: reference
---

Normally WPA Supplicant file is located at:
{% highlight ruby %}
/etc/wpa_supplicant/wpa_supplicant.conf
{% endhighlight %}

You can easily edit the file by using nano:
{% highlight ruby %}
sudo nano /etc/wpa_supplicant/wpa_supplicant.conf
{% endhighlight %}

or vim:
{% highlight ruby %}
sudo vim /etc/wpa_supplicant/wpa_supplicant.conf
{% endhighlight %}

The default format for the file is:
{% highlight ruby %}
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=<Insert 2 letter ISO 3166-1 country code here>

network={
 ssid="<Name of your wireless LAN>"
 psk="<Password for your wireless LAN>"
}
{% endhighlight %}

Reference for country code [here](https://en.wikipedia.org/wiki/ISO_3166-1){:target="_blank"}



