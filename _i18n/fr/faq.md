# Sommaire

* [I. Erreurs liées à youtube-dl](#i-erreurs-liées-à-youtube-dl)


# I. Erreurs liées à youtube-dl

Dans Catch-Up TV & More nous utilisons le module **script.module.youtube-dl** dans deux cas:
* Le mode téléchargement (il permet de télécharger les contenus proposés par les replays et les sites web)
* La lecture des vidéos hébergées par youtube.com, dailymotion.com, vimeo.com, ...

Le module **script.module.youtube-dl** (developpée par Ruuk) permet d'utiliser l'application bien connue **youtube-dl** dans Kodi.

>* **script.module.youtube-dl:** <https://github.com/ruuk/script.module.youtube.dl/>
>* **youtube-dl:** <https://github.com/ytdl-org/youtube-dl>

Ce module n'est mis à jour que de temps en temps (peut être 4 fois par an) donc il est possible de rencontrer des erreurs.

Si vous obtenez des notifications d'erreur de youtube-dl durant la lecture d'une video dans Catch-up TV & More et que cette même vidéo est lue sans erreur dans votre navigateur web, nous vous invitons à effectuer ce **workaround**.
Ce **workaround** va permettre de mettre à jour les fichiers de la dernière version de **youtube-dl** dans l'extension **script.module.youtube-dl**.

Cette extension est présente dans le dossier `addons` de Kodi dont chemin dépend de votre plate-forme :
* **Windows :** `C:\Users\[user]\AppData\Roaming\Kodi\addons`
* **Linux :** `/home/[user]/.kodi/addons`
* **macOS :** `/Users/[user]/Library/Application Support/Kodi/addons`
* **Android :** `/sdcard/Android/data/org.xbmc.kodi/files/.kodi/addons`
* **LibreELEC :** `/storage/.kodi/addons`
* **Shield Android TV:** `/internal/Android/data/org.xbmc.kodi/files/.kodi/addons`
* **Amazon Fire:** `/External storage/Android/Data/org.xbmc.kodi/files/.kodi/addon`

Après avoir trouvé le dossier `addons`, vous devez supprimer tous les fichiers et repertoires présent dans le dossier `addons/script.module.youtube.dl/lib/youtube_dl`.

Vous pouvez ensuite vous rendre à cette URL <https://github.com/ytdl-org/youtube-dl/releases> pour télécharger la dernière version de **youtube-dl**. Le fichier à télécharger est *"Source code (zip)"*. Ouvrir ensuite le fichier zip téléchargé, aller dans le repertoire *"youtube_dl"* présent dans ce zip et copier/coller tous le contenu de ce dossier dans le dossier `addons/script.module.youtube.dl/lib/youtube_dl` de l'extension à mettre à jour.

Pour finir, vous pouvez tester de nouveau la vidéo remontant une erreur. Si l'erreur est toujours présente, nous vous invitons à ouvrir une **issue** à cette URL <https://github.com/Catch-up-TV-and-More/plugin.video.catchuptvandmore/issues>.