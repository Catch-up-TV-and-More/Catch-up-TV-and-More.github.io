> ⚠️ This feature is only available on Kodi Leia (18) version and above.

# Summary

* [Introduction](#introduction)
* [I. Prerequisites](#i-prerequisites)
* [II. Installing "IPTV Manager"](#ii-installing-iptv-manager)
* [III. Enable channels](#iii-enable-channels)
* [IV. Recording Lives TV](#iv-recording-lives-tv)
    * [1. Prerequisites and limitations](#1-prerequisites-and-limitations)
    * [2. Installing "IPTV Recorder"](#2-installing-iptv-recorder)
    * [3. Configuring and using "IPTV Recorder"](#3-configuring-and-using-iptv-recorder)

# Introduction

Since version 0.2.30 of the addon it is possible to access the different live TV streams offered in Catch-up TV & More directly from the Kodi "Live TV" feature.
This feature uses the IPTV Manager addon as well as the PVR IPTV Simple.


This feature has several advantages (non-exhaustive list):

* Take full advantage of the TV guide managed by Kodi
* Organize different channels into groups
* One place to group the channels of other PVR and video addons (TNT, Satellite, ...)

A preview of the final result once you have followed this tutorial:

![](/img/live_tv_installation/intro1.jpeg)

![](/img/live_tv_installation/intro2.jpeg)

![](/img/live_tv_installation/intro3.jpeg)

![](/img/live_tv_installation/intro4.jpeg)


# I. Prerequisites

If you have not already done so, it is necessary to proceed with the installation of Catch-up TV & More in order to take advantage of this feature. Just follow this [tutorial](https://catch-up-tv-and-more.github.io/en/installation/) before continuing here.

Some channels require to have a user account to access their service.
The first thing to do is to create the accounts necessaries directly on the websites of concerned channels.
Finally, it is required to fill your credentials in the parameters of the addon.

Open Catch-up TV & More.

![](/img/live_tv_installation/accounts1.jpeg)

Access the settings of the add-on by pressing the left arrow on your keyboard or remote control.

![](/img/live_tv_installation/accounts2.jpeg)

Finally, go to the "Accounts" tab and fill in your username and password for the desired channels.
Do not forget to confirm with the "OK" button to save your settings.

![](/img/live_tv_installation/accounts3.jpeg)

# II. Installing "IPTV Manager"

It is first necessary to install IPTV Manager.
To do this, go to the Catch-up TV & More settings in the "TV Integration" section and choose "Install IPTV Manager add-on".

![](/img/live_tv_installation/install_iptvmanager_0.jpeg)

![](/img/live_tv_installation/install_iptvmanager_1.jpeg)


# III. Enable channels

Once IPTV Manager is installed, go back to the Catch-up TV & More settings to select the channels you want to appear in the Kodi TV section.
This is done in the "TV Integration" section by choosing "Select channels to enable".
Don't forget to save your settings by clicking the "OK" buttons.

![](/img/live_tv_installation/select_channels_0.jpeg)

![](/img/live_tv_installation/select_channels_1.jpeg)

If your channels still do not appear in the "TV" section of Kodi you can perform the following steps in the IPTV Manager settings:

1. "IPTV Simple" --> "Configure IPTV Simple automatically..."
2. "Channels" --> "Refresh channels and guide now..."

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