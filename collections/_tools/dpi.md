---
layout: minimal
title: "DPi"
permalink: /tools/dpi
description: "A Designer Kit for Raspberry Pi."
introduction: DPi is custom made Raspberry Pi system, ready for designer to start prototyping a connected product.
type: RPi
---

Available soon via the Bucket!

See the development of our DPi generator [here](https://github.com/datacentricdesign/raspbian-dist)

DPi is custom made Raspberry Pi system, ready for designer to start prototyping a connected product. When creating a new Thing in your Data Bucket, select 'DPi' as
type. It will prompt you for some additional information such as user credentials
and network. After a few minutes, you will receive an email to download your DPi image, ready to go!

## Getting started fast, remotely and with security 

Raspberry Pi settings can be combersome when getting started. DPi enables SSH, disables auto-login and sets your own, secured network credentials so that you can directly access your pi remotely without a monitor/keyboard/mouse.


## Sending data to the cloud, from the first minute!

DPi embbed a private key which has a public key registered on Bucket, attached to your registered Thing. It means that DPi is automatically able to send and receive data from Bucket, out of the box! By default, it shares its CPU usage every minute (for demonstration purposes) and its IP address (convenient on some large network to locate your Raspberry Pi).

## Eduroam ready

If you fill in your university credentials, it setups the connection to Eduroam so that you can get started on campus.

## Hot Spot

Designing your connected product, you might want to rely on a WiFi network that you fully control. DPi comes with all the necessary libraries to quickly start your on WiFi network, directly on the Raspberry Pi. In this setting you will need an ethernet
connection to access the Internet.


## Customizations 
* Reconfiguration of network driver launch, and automatic configuration of supplicant file to work with eduroam with supplied credentials
* Raspbian setup:
  * SPI & I2C enabled by default
  * SSH access on, autologin disabled 
  * Lite version of raspbian with a few extra installs (stopped stage 5 of raspbian)
* Installed all DCD python dependencies 
* Several ancillary/stale items are removed, including python2
* Custom service scripts preinstalled in, with embedded thing keys in each folder. 
  * `/etc/systemd/system/service_scripts/` 
  * `/etc/systemd/system/service_scripts/python/`
