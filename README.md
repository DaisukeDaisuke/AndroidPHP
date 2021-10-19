# AndroidPHP

select language
-  english
- [日本語](https://github.com/DaisukeDaisuke/AndroidPHP_old/blob/master/README_JP.md)

select version(coming soon)
- Android 4-6
- Android 7+
- [Raspberry Pi 3b](https://github.com/DaisukeDaisuke/AndroidPHP_old/blob/master/RaspberryPi.md) (experimental)
## Android 4-6(and more)
This is a php binary for PocketMine-MP.  
For using it on Android, need a terminal emulator.
### 
## note
This php binary is for 64bit.  
Please note that 32bit will not work.  
**This method has been tested on Android6 and Raspberry Pi 3b only and may not work on newer Android versions.**

This php binary can still connect to the Internet.  
Also, the Raspberry Pi can connect to the Internet as is.  
To connect to the Internet on Android, you need to prepare resolv.conf and cacert.pem, which can be found in the download link in the description below.    
To run the server on Android, you need to prepare PMMP by yourself.

## Required Applications
In this section, we will use "Android Terminal Emulator" as a terminal emulator.

https://play.google.com/store/apps/details?id=jackpal.androidterm

## Installing php
### Download php
The PHP can be downloaded from the [This release page](https://github.com/DaisukeDaisuke/AndroidPHP/releases).

![img1](https://user-images.githubusercontent.com/17798680/73345192-f9324300-42c6-11ea-9036-c162bf03c5bd.png)

## Installing php
Please execute the following command.  
To paste text from the clipboard, press and hold the screen in the "Android Terminal Emulator" application, and please select "Paste".
```
cp /storage/emulated/0/Download/php /data/data/jackpal.androidterm/app_HOME/php
chmod 777 /data/data/jackpal.androidterm/app_HOME/php
```

## Download various files to connect to the Internet
Please Download the various files (resolv.conf, cacert.pem, php.ini) from the following download links.

#### direct downloads
- [cacert.pem](https://curl.haxx.se/ca/cacert.pem)
- [resolv.conf](https://www.dropbox.com/s/xwta1aobds1557e/resolv.conf?dl=1)
- [php.ini](https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/php.ini)

## Placing the various files
Please copy all the downloaded files `cacert.pem`, `resolv.conf`, and `php.ini` to the `/storage/emulated/0/PocketMine/config/` folder.

## Install PocketMine-MP
Please download "PocketMine-MP.phar" from the following link and copy it to "/storage/emulated/0/PocketMine/".
https://github.com/pmmp/PocketMine-MP/releases/latest/download/PocketMine-MP.phar

## launch PocketMine-MP
Launch "Android Terminal Emulator" downloaded from Google Play, and execute the following command.
```
cd /storage/emulated/0/PocketMine/
env LESMI_RESOLV_CONF_DIR=/storage/emulated/0/PocketMine/config/resolv.conf SSL_CERT_FILE=/storage/emulated/0/PocketMine/config/cacert.pem /data/data/jackpal.androidterm/app_HOME/php -c /storage/emulated/0/PocketMine/config/php.ini /storage/emulated/0/PocketMine/PocketMine-MP.phar
```
The LESMI_RESOLV_CONF_DIR environment variable is created by the modified musl (gcc).

<hr />

#### Other information
<details>
<summary>A url that links directly to the latest binary.</summary>
<br>

```
pm3
https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/php
https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/php-gd
https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/php-gd-no-modification
pm3-zip
https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/php.zip
https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/zip-php-gd.zip
https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/zip-php-gd-no-modification.zip
php.ini
https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/php-pm4.ini
pm4
https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/php-pm4-gd
pm4-zip
https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/php-pm4-gd.zip
php.ini
https://github.com/DaisukeDaisuke/AndroidPHP/releases/latest/download/php.ini
```
</details>

