# Summary

* [I. Issues related to youtube-dl](#i-issues-related-to-youtube-dl)


# I. Issues related to youtube-dl

In Catch-Up TV & More, we use the add-on **script.module.youtube-dl** for two cases:
* Download mode (Download catch-up TV and website contents)
* Play contents hosted by youtube.com, dailymotion.com, vimeo.com, ...

The add-on **script.module.youtube-dl** (developped by Ruuk) is a Kodi wrapper of the well known application **youtube-dl**.

>* **script.module.youtube-dl:** <https://github.com/ruuk/script.module.youtube.dl/>
>* **youtube-dl:** <https://github.com/ytdl-org/youtube-dl>

It is updated time to time (maybe 4 times a year) so it might happens some issues.

If you have a notification indicating an issue with youtube-dl during playing one content with Catch-up TV & More and if this same content is playable in your browser. You can try the workaround below.
This **workaround** will allow to update the files of the last version of **youtube-dl** into the add-on **script.module.youtube-dl**.

This add-on is located in the `addons` folder of Kodi.
The location of this folder depends on your platform:
* **Windows:** `C:\Users\[user]\AppData\Roaming\Kodi\addons`
* **Linux:** `/home/[user]/.kodi/addons`
* **macOS:** `/Users/[user]/Library/Application Support/Kodi/addons`
* **Android:** `/sdcard/Android/data/org.xbmc.kodi/files/.kodi/addons`
* **LibreELEC:** `/storage/.kodi/addons`
* **Shield Android TV:** `/internal/Android/data/org.xbmc.kodi/files/.kodi/addons`
* **Amazon Fire:** `/External storage/Android/Data/org.xbmc.kodi/files/.kodi/addon`

After finding this folder, you need to remove all files and directories presents in the folder `addons/script.module.youtube.dl/lib/youtube_dl`.

Then, go to this URL <https://github.com/ytdl-org/youtube-dl/releases> to download the last release of **youtube-dl**. The file to download is *"Source code (zip)"*. Open the downloaded zip file, go to the folder *"youtube_dl"* and copy/paste all contains of this folder into the folder `addons/script.module.youtube.dl/lib/youtube_dl`.

Finally, you can try again to play the content. If the issue is still present do not hesitate to open an issue at the URL <https://github.com/Catch-up-TV-and-More/plugin.video.catchuptvandmore/issues>.