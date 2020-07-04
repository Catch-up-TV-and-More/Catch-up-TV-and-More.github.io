> ⚠️ For the moment this functionality has only been tested under Kodi Leia (18)

# Summary

* [Introduction](#introduction)
* [I. Prerequisites](#i-prerequisites)
* [II. PVR "IPTV Simple Client"](#ii-pvr-iptv-simple-client)
    * [1. Installing "PVR IPTV Simple Client"](#1-installing-pvr-iptv-simple-client)
    * [2. Configuring "PVR IPTV Simple Client"](#2-configuring-pvr-iptv-simple-client)
* [III. Organization of channels and groups of channels](#iii-organization-of-channels-and-groups-of-channels)
    * [1. Selecting the channels group](#1-selecting-the-channels-group)
    * [2. Managing channels and groups](#2-managing-channels-and-groups)
* [IV. Recording Lives TV](#iv-recording-lives-tv)
    * [1. Prerequisites and limitations](#1-prerequisites-and-limitations)
    * [2. Installing "IPTV Recorder"](#2-installing-iptv-recorder)
    * [3. Configuring and using "IPTV Recorder"](#3-configuring-and-using-iptv-recorder)

# Introduction

Since version 0.2.5 of the add-on it is possible to use the "TV" feature of Kodi to directly access the different live TV streams offered in Catch-up TV & More.

This feature has several advantages (non-exhaustive list):

* Take full advantage of the TV guide managed by Kodi
* Organize different channels into groups
* One place to group the channels of other PVR (TNT, Satellite, ...)
* If a new TV channel is available in the add-on via an update, it is also available in the TV section of Kodi

A preview of the final result once you have followed this tutorial:

![](/img/live_tv_installation/intro1.jpeg)

![](/img/live_tv_installation/intro2.jpeg)

![](/img/live_tv_installation/intro3.jpeg)

![](/img/live_tv_installation/intro4.jpeg)


# I. Prerequisites

If you have not already done so, it is necessary to proceed with the installation of Catch-up TV & More in order to take advantage of this feature. Just follow this [tutorial](https://catch-up-tv-and-more.github.io/en/installation/) before continuing here.

Some channels require to have a user account to access their service.
The first thing to do is to create the accounts necessaries directly on the websites of concerned channels.
Finally, it is required to fill your credentials in the parameters of the add-on.

Open Catch-up TV & More.

![](/img/live_tv_installation/accounts1.jpeg)

Access the settings of the add-on by pressing the left arrow on your keyboard or remote control.

![](/img/live_tv_installation/accounts2.jpeg)

Finally, go to the "Accounts" tab and fill in your username and password for the desired channels.
Do not forget to confirm with the "OK" button to save your settings.

![](/img/live_tv_installation/accounts3.jpeg)

# II. PVR "IPTV Simple Client"

## 1. Installing "PVR IPTV Simple Client"

The "TV" feature of Kodi requires the use of a PVR.
In our case we will use the PVR "IPTV Simple Client".

> IPTV Simple Client will serve as a bridge between Kodi TV and the add-on Catch-up TV & More. <br>
> Indeed, we will provide the PVR a *m3u* file containing entries for each available channel in the add-on. <br>
> Each entry of this file associates a name of channel (*for example France 2*) with the Python file corresponding to this channel in the plugin (*`plugin://plugin.video.catchuptvandmore/main/live_bridge/?item_id=france-2&item_module=resources.lib.channels.fr.francetv`*). <br>
> So, when a channel is selected in Kodi TV, this last call in background Catch-up TV & More which deals with recovering the video stream before transmitting it back to Kodi which opens the player with the requested channel .

If Kodi is installed on Linux, you need to first install the PVR on your system with the command `apt-get install kodi-pvr-iptvsimple`.

To install "PVR IPTV Simple Client", open "Add-ons".

![](/img/live_tv_installation/iptv1.jpeg)

Then choose the open cardboard logo.

![](/img/live_tv_installation/iptv2.jpeg)

Install from repository.

![](/img/live_tv_installation/iptv3.jpeg)

PVR clients.

![](/img/live_tv_installation/iptv4.jpeg)

Select PVR IPTV Simple Client.

![](/img/live_tv_installation/iptv5.jpeg)

If it's not installed, install-it.

![](/img/live_tv_installation/iptv6.jpeg)

## 2. Configuring "PVR IPTV Simple Client"

It is now necessary to configure IPTV Simple Client.

![](/img/live_tv_installation/iptv8.jpeg)

The first thing to do is to give IPTV Simple Client the *m3u* file to use, which is the list of channels you want to appear in Kodi TV.

In the "General" tab choose "Local path" for the location (1).

Finally, select "M3U Play List Path" to open the Kodi File Explorer (2).

![](/img/live_tv_installation/iptv9.jpeg)

The *m3u* files of each country are in the `m3u` folder present in the add-on folder (`plugin.video.catchuptvandmore`).
This folder `m3u` is hidden by default in Kodi. You need to activate the option **Show hidden files and directories** present "System > Media" to have access to these *m3u* files.

The Kodi `addons` folder depends on your platform:

* **Windows:** `C:\Users\[user]\AppData\Roaming\Kodi\addons`
* **Linux:** `/home/[user]/.kodi/addons`
* **macOS:** `/Users/[user]/Library/Application Support/Kodi/addons`
* **Android:** `/sdcard/Android/data/org.xbmc.kodi/files/.kodi/addons`
* **LibreELEC:** `/storage/.kodi/addons`
* **Shield Android TV:** `/internal/Android/data/org.xbmc.kodi/files/.kodi/addons`
* **Amazon Fire:** `/External storage/Android/Data/org.xbmc.kodi/files/.kodi/addon`

For others, you can find your *"special://home"* [here](https://kodi.wiki/view/Special_protocol#Default_OS_mappings).

Finally, go in the `m3u` folder by following this path:

* `plugin.video.catchuptvandmore/resources/m3u`

Now you can choose the *m3u* file of you favourite country.

![](/img/live_tv_installation/iptv11.jpeg)

> the file `live_tv_all.m3u` contains channels of all available countries.

Some countries have TV guides with XMLTV files.
These files allow Kodi to display the schedules and program descriptions of your TV channels.

Go to the "EPG Settings" tab of the PVR IPTV Simple Client settings and select "XMLTV URL".

![](/img/live_tv_installation/iptv12.jpeg)

Finally copy and paste your country guide (again, the `tv_guide_all` guide contains all TV guides of all available countries)

* **France:** `http://bit.ly/tvguidefr`
* **Belgium:** `http://bit.ly/tvguidebe`
* **Italy:** `http://bit.ly/tvguideit`
* **United Kingdom:** `http://bit.ly/tvguideunitedkingdom`
* **All available countries:** `http://bit.ly/tvguideall`

> Programs may not be available for all channels

> If the timezone of the XMLTV file is different from yours, you can adjust it using the "EPG Time Shift" setting

Finally, confirm the settings.

![](/img/live_tv_installation/iptv13.jpeg)

![](/img/live_tv_installation/iptv14.jpeg)

![](/img/live_tv_installation/iptv13.jpeg)

**You must now restart Kodi**

# III. Organization of channels and groups of channels

## 1. Selecting the channels group

You have the option to choose which channel group to display in Kodi TV.

To do this, open "TV" and use the left arrow on your keyboard or remote control to access the group selection

![](/img/live_tv_installation/group1.jpeg)

![](/img/live_tv_installation/group2.jpeg)

![](/img/live_tv_installation/group3.jpeg)

## 2. Managing channels and groups

You can also edit and/or hide the different groups of channels.
Also, it is possible to change the order of the strings.

To access channel and group managers simply follow the directions below.

![](/img/live_tv_installation/manage1.jpeg)

![](/img/live_tv_installation/manage2.jpeg)

![](/img/live_tv_installation/manage3.jpeg)

![](/img/live_tv_installation/manage4.jpeg)

# IV. Recording Lives TV

The PVR IPTV Simple does not provide the functionnality to record lives TV.
This part of the documentation will details all steps to add this functionnality easily.
Other PVR's exist (like "TVHeadend, ...), which offer natively to record lives TV but required a backend deployed to work.

## 1. Prerequisites and limitations

The list of prerequisites are:

* FFMPEG installed on the operating system used by Kodi (Windows, Linux, Raspbian, libreelec ...) - This tutorial will not explain this topic but you can find easily in the internet how to install it if it not present in your environment.
* The m3u file of Catch-up TV & More configured in the PVR IPTV Simple

Les limitations are:

* IPTV Recorder does not permit to block the standby mode of Kodi instance during a recording ongoing or to wake up Kodi instance when a recording will start.
* On Android, the deployement of FFMPEG is difficult. It is not present by default on the Play Store.
* IPTV Recorder does not permit to record lives TV protected by DRM. If you test to record it, Kodi instance is stuck in some way and you may need to kill it.

## 2. Installing "IPTV Recorder"

Download et install the repository **repository.primaeval-0.0.2** present at this url <https://github.com/primaeval/repository.primaeval/raw/master/zips/repository.primaeval/repository.primaeval-0.0.2.zip>

![](/img/live_tv_installation/iptvrecorder01.jpeg)

![](/img/live_tv_installation/iptvrecorder02.jpeg)

![](/img/live_tv_installation/iptvrecorder03.jpeg)

Go to the directory where this zip file **repository.primaeval-0.0.2.zip** is stored

Click on "OK" to install this repository

![](/img/live_tv_installation/iptvrecorder04.jpeg)

Install the add-on IPTV Recoder available on "Video Add-ons" from this newly installed repository.

![](/img/live_tv_installation/iptvrecorder05.jpeg)

![](/img/live_tv_installation/iptvrecorder06.jpeg)

![](/img/live_tv_installation/iptvrecorder07.jpeg)

![](/img/live_tv_installation/iptvrecorder08.jpeg)

![](/img/live_tv_installation/iptvrecorder09.jpeg)

## 3. Configuring and using "IPTV Recorder"

Go to the settings of the add-on "IPTV Recorder" to fill the path of the executable of FFMPEG

![](/img/live_tv_installation/iptvrecorder10.jpeg)

![](/img/live_tv_installation/iptvrecorder11.jpeg)

You have also the setting of the path where the recording will be stored. By default, the repository is **special://temp** (It is a variable of Kodi <https://kodi.wiki/view/Special_protocol>)

Go to the menu of this add-on to choose the program to record

Open the add-on "IPTV Recorder"

![](/img/live_tv_installation/iptvrecorder12.jpeg)

Go to "Channels Group"

![](/img/live_tv_installation/iptvrecorder13.jpeg)

Choose the program to record

![](/img/live_tv_installation/iptvrecorder14.jpeg)

![](/img/live_tv_installation/iptvrecorder15.jpeg)

![](/img/live_tv_installation/iptvrecorder16.jpeg)

![](/img/live_tv_installation/iptvrecorder17.jpeg)

Go back to the principal menu of "IPTV Recorder" and go to the "Recordings" menu. You will find all recordings in progress and finished.

![](/img/live_tv_installation/iptvrecorder18.jpeg)

![](/img/live_tv_installation/iptvrecorder19.jpeg)

At the end of the recording, you will find it at this place "**special://temp**" (if not changed previously) or throught the add-on "IPTV Recoder". You could add this directory to the video sources of Kodi instance.

![](/img/live_tv_installation/iptvrecorder20.jpeg)

![](/img/live_tv_installation/iptvrecorder21.jpeg)

![](/img/live_tv_installation/iptvrecorder22.jpeg)