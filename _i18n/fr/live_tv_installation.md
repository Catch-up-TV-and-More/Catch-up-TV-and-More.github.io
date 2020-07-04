> ⚠️ Pour l'instant cette fonctionnalité a seulement été testé sous Kodi Leia (18)

# Sommaire

* [Introduction](#introduction)
* [I. Prérequis](#i-prérequis)
* [II. PVR "IPTV Simple Client"](#ii-pvr-iptv-simple-client)
    * [1. Installation de "PVR IPTV Simple Client"](#1-installation-de-pvr-iptv-simple-client)
    * [2. Configuration de "PVR IPTV Simple Client"](#2-configuration-de-pvr-iptv-simple-client)
* [III. Organisation des chaînes et groupes de chaînes](#iii-organisation-des-chaînes-et-groupes-de-chaînes)
    * [1. Sélection du groupe de chaînes](#1-sélection-du-groupe-de-chaînes)
    * [2. Gestion des chaînes et des groupes](#2-gestion-des-chaînes-et-des-groupes)
* [IV. Enregistrement des directs TV](#iv-enregistrement-des-directs-tv)
    * [1. Prérequis et Limitations](#1-prérequis-et-limitations)
    * [2. Installation de IPTV Recorder](#2-installation-de-iptv-recorder)
    * [3. Configuration et utilisation de IPTV Recorder](#3-configuration-et-utilisation-de-iptv-recorder)

# Introduction

Depuis la version 0.2.5 de l'add-on il est possible d'utiliser la fonctionnalité "TV" de Kodi afin d'accéder directement aux différents flux TV en direct proposés dans Catch-up TV & More.

Cette fonctionnalité a plusieurs avantages (liste non exhaustive) :

* Profiter pleinement du guide TV géré par Kodi
* Organiser les différentes chaînes dans des groupes
* Un seul endroit pour regrouper les chaînes des autres PVR (TNT, Satellite, ...)
* Si une nouvelle chaîne TV est disponible dans l'add-on via une mise à jour, elle l'est aussi dans la section TV de Kodi

Un petit aperçu du résultat final une fois que vous aurez suivi ce tutoriel :

![](/img/live_tv_installation/intro1.jpeg)

![](/img/live_tv_installation/intro2.jpeg)

![](/img/live_tv_installation/intro3.jpeg)

![](/img/live_tv_installation/intro4.jpeg)


# I. Prérequis

Si vous ne l'avez pas encore fait, il est nécessaire de procéder à l'installation de Catch-up TV & More afin de profiter de cette fonctionnalité. Suivez simplement ce [tutoriel](https://catch-up-tv-and-more.github.io/fr/installation/) avant de continuer ici.

Certaines chaînes nécessitent d'avoir un compte utilisateur afin de profiter de leur service (c'est par exemple le cas de 6play).
Le première chose à faire est de créer le(s) compte(s) nécessaire(s) directement sur le(s) site(s) internet des chaînes concernées.
Enfin, il est faut renseigner vos couples identifiants/mots de passe dans les paramètres de l'add-on.

Ouvrez Catch-up TV & More.

![](/img/live_tv_installation/accounts1.jpeg)

Accédez aux paramètres de l'add-on en appuyant sur la flèche gauche de votre clavier ou télécommande.

![](/img/live_tv_installation/accounts2.jpeg)

Enfin, rendez-vous dans l'onglet "Comptes" et renseignez vos identifiants et mots de passe pour les chaînes désirées.
N'oubliez pas de valider avec le bouton "OK" afin de sauvegarder vos réglages.

![](/img/live_tv_installation/accounts3.jpeg)


# II. PVR "IPTV Simple Client"

## 1. Installation de "PVR IPTV Simple Client"

La fonctionnalité "TV" de Kodi nécessite l'utilisation d'un PVR (Client enregistreur vidéo).
Dans notre cas nous allons utiliser le PVR "IPTV Simple Client".

> Ce dernier va servir de pont entre la TV de Kodi et l'add-on Catch-up TV & More. <br>
> En effet, nous allons fournir au PVR un fichier *m3u* contenant une entrée différente pour chaque chaîne disponible dans l'add-on. <br>
> Chaque entrée de ce fichier associe un nom de chaîne (*par exemple France 2*) au fichier Python correspondant à cette chaîne dans le plugin (*`plugin://plugin.video.catchuptvandmore/main/live_bridge/?item_id=france-2&item_module=resources.lib.channels.fr.francetv`*). <br>
> Ainsi, quand une chaîne est sélectionnée dans la TV de Kodi, ce dernier appel en fond Catch-up TV & More qui s'occupe de récupérer le flux vidéo avant de le transmettre en retour à Kodi qui ouvre le lecteur avec la chaîne demandée.

Si Kodi est installé sous Linux, vous devez préalablement installer le PVR sur votre système avec la commande `apt-get install kodi-pvr-iptvsimple`.

Pour installer "PVR IPTV Simple Client", ouvrir "Extensions".

![](/img/live_tv_installation/iptv1.jpeg)

Choisir en suite le logo du carton ouvert.

![](/img/live_tv_installation/iptv2.jpeg)

Installer depuis un dépôt.

![](/img/live_tv_installation/iptv3.jpeg)

Clients enregistreur vidéo.

![](/img/live_tv_installation/iptv4.jpeg)

Sélectionner PVR IPTV Simple Client.

![](/img/live_tv_installation/iptv5.jpeg)

Si ce PVR n'est pas déjà installé, installez-le.

![](/img/live_tv_installation/iptv6.jpeg)

## 2. Configuration de "PVR IPTV Simple Client"

Il est maintenant nécessaire de le configurer.

![](/img/live_tv_installation/iptv8.jpeg)

La première chose à faire est de donner à IPTV Simple Client le fichier *m3u* à utiliser, c'est-à-dire la liste des chaînes que vous souhaitez voir apparaître dans la TV de Kodi.

Dans l'onglet "Général" choisissez déjà "Chemin local" pour l'emplacement (1).

Enfin, sélectionnez "Chemin de la liste de chaînes M3U" afin d'ouvrir l'explorateur de fichiers de Kodi (2).

![](/img/live_tv_installation/iptv9.jpeg)

Les fichiers *m3u* de chaque pays sont disponibles dans le dossier `m3u` présent dans le dossier du plugin (`plugin.video.catchuptvandmore`).
Ce dossier `m3u` est caché par défaut dans Kodi. L'option **Afficher les dossiers et les fichiers cachés** disponible dans "Système > Médias" doit être activée pour avoir accès aux fichiers *m3u*.

Pour ce rendre dans le dossier `addons` de Kodi le chemin dépend de votre plate-forme :

* **Windows :** `C:\Users\[user]\AppData\Roaming\Kodi\addons`
* **Linux :** `/home/[user]/.kodi/addons`
* **macOS :** `/Users/[user]/Library/Application Support/Kodi/addons`
* **Android :** `/sdcard/Android/data/org.xbmc.kodi/files/.kodi/addons`
* **LibreELEC :** `/storage/.kodi/addons`
* **Shield Android TV:** `/internal/Android/data/org.xbmc.kodi/files/.kodi/addons`
* **Amazon Fire:** `/External storage/Android/Data/org.xbmc.kodi/files/.kodi/addon`

Pour les autres cas, vous trouverez votre *"special://home"* [ici](https://kodi.wiki/view/Special_protocol#Default_OS_mappings).

Enfin, rendez-vous dans le dossier `m3u` en suivant ce chemin :

* `plugin.video.catchuptvandmore/resources/m3u`

Vous pouvez alors choisir le fichier *m3u* de votre pays favori.

![](/img/live_tv_installation/iptv11.jpeg)

> Le fichier `live_tv_all.m3u` est une compilation des chaînes de tous les pays disponibles.

Certains pays disposent de guides TV sous la forme de fichiers XMLTV.
Ces fichiers permettent à Kodi d'afficher les horaires et descriptions des programmes de vos chaînes TV.

Rendez-vous dans l'onglet "Guide TV" des paramètres de PVR IPTV Simple Client et sélectionnez "URL du fichier XML".

![](/img/live_tv_installation/iptv12.jpeg)

Enfin faites un copier-coller du guide de votre pays (ici encore, le guide `tv_guide_all` est une compilation des guides TV de tous les pays disponibles)

* **France :** `http://bit.ly/tvguidefr`
* **Belgique :** `http://bit.ly/tvguidebe`
* **Italie:** `http://bit.ly/tvguideit`
* **Royaume-Uni:** `http://bit.ly/tvguideunitedkingdom`
* **Tous les pays disponibles :** `http://bit.ly/tvguideall`

> Les programmes ne sont pas forcément disponibles pour toutes les chaînes

> Si le fuseau horaire du fichier XMLTV est différent du votre, vous pouvez l'ajuster grâce à l'option "Différé du guide des programmes"

Finalement, validez les paramètres.

![](/img/live_tv_installation/iptv13.jpeg)

![](/img/live_tv_installation/iptv14.jpeg)

![](/img/live_tv_installation/iptv13.jpeg)

**Vous devez maintenant redémarrer Kodi**

# III. Organisation des chaînes et groupes de chaînes

## 1. Sélection du groupe de chaînes

Vous avez la possibilité de choisir quel groupe de chaînes à afficher dans la TV de Kodi.

Pour cela, ouvrez "TV" et utiliser la flèche gauche de votre clavier ou télécommande afin d'accéder à la sélection du groupe

![](/img/live_tv_installation/group1.jpeg)

![](/img/live_tv_installation/group2.jpeg)

![](/img/live_tv_installation/group3.jpeg)


## 2. Gestion des chaînes et des groupes

Vous pouvez aussi modifier et/ou masquer les différents groupes de chaînes.
De même, il est possible de modifier l'ordre des chaînes.

Pour accéder aux gestionnaires des chaînes et groupes suivez simplement les indications ci-dessous.

![](/img/live_tv_installation/manage1.jpeg)

![](/img/live_tv_installation/manage2.jpeg)

![](/img/live_tv_installation/manage3.jpeg)

![](/img/live_tv_installation/manage4.jpeg)

# IV. Enregistrement des directs TV

Le PVR IPTV Simple ne propose pas la fonctionnalité d'enregistrement des directs TV.
Cette partie va détailler les étapes pour ajouter cette fonctionnalité via une méthode simple et ne demandant pas d'installer un service de type "serveur backend".
Il existe d'autres PVR par exemple "TVHeadend, ..." qui proposent en natif de gérer l'enregistrement mais qui sont beaucoup plus complexes à mettre en oeuvre.

## 1. Prérequis et Limitations

La liste des prérequis est la suivante:

* FFMPEG installé - Nous ne détaillerons pas comment l'installer dans ce tutoriel mais vous pouvez trouver cette information via des recherches sur internet suivant votre système d'exploitation (Windows, Linux, etc ...).
* Le fichier m3u provenant de Catch-up TV & More configuré dans le PVR IPTV Simple

Les limitations sont:

* IPTV Recorder ne permet pas de bloquer la mise en veille de Kodi même si l'enregistrement est en cours ou de sortir de la mise en veille quand l'enregistrement débute.
* Sur Android, le binaire FFMPEG est difficile à déployer. Il n'existe pas dans le Play Store d'Android.
* IPTV Recorder ne permet pas d'enregistrer des directs TV protégés par DRM. Si on test d'enregistrer un direct TV protégé par DRM nous avons le sablier de chargement de Kodi en permanence (tuer l'application kodi est donc nécessaire dans ce cas).

## 2. Installation de IPTV Recorder

Télécharger et installer le **repository.primaeval-0.0.2** présent à cette url <https://github.com/primaeval/repository.primaeval/raw/master/zips/repository.primaeval/repository.primaeval-0.0.2.zip>

![](/img/live_tv_installation/iptvrecorder01.jpeg)

![](/img/live_tv_installation/iptvrecorder02.jpeg)

![](/img/live_tv_installation/iptvrecorder03.jpeg)

Aller dans le repertoire où vous avez sauvegarder le fichier zip **repository.primaeval-0.0.2.zip**

Cliquer sur "OK" pour installer ce repository

![](/img/live_tv_installation/iptvrecorder04.jpeg)

Installer l'extension IPTV Recoder présente dans la section "Vidéo Extensions" depuis le dépôt de primeval

![](/img/live_tv_installation/iptvrecorder05.jpeg)

![](/img/live_tv_installation/iptvrecorder06.jpeg)

![](/img/live_tv_installation/iptvrecorder07.jpeg)

![](/img/live_tv_installation/iptvrecorder08.jpeg)

![](/img/live_tv_installation/iptvrecorder09.jpeg)

## 3. Configuration et utilisation de IPTV Recorder

Accéder aux options de configuration du plugin IPTV Recorder afin de renseigner le chemin de l'application FFMPEG

![](/img/live_tv_installation/iptvrecorder10.jpeg)

![](/img/live_tv_installation/iptvrecorder11.jpeg)

Vous avez aussi l'option pour renseigner le répertoire de destination des enregistrements. Par défault, le repertoire est **special://temp** (c'est une variable Kodi <https://kodi.wiki/view/Special_protocol>)

Accéder au menu de l'extension pour choisir le programme à enregister

Ouvrir l'extension IPTV Recorder

![](/img/live_tv_installation/iptvrecorder12.jpeg)

Aller dans le menu "Groupe de chaînes"

![](/img/live_tv_installation/iptvrecorder13.jpeg)

Choisir le programme à enregistrer

![](/img/live_tv_installation/iptvrecorder14.jpeg)

![](/img/live_tv_installation/iptvrecorder15.jpeg)

![](/img/live_tv_installation/iptvrecorder16.jpeg)

![](/img/live_tv_installation/iptvrecorder17.jpeg)

Revenir sur le menu principal de IPTV Recorder et aller dans le menu "Enregistrements". Vous trouverez les enregistrements en cours et terminés.

![](/img/live_tv_installation/iptvrecorder18.jpeg)

![](/img/live_tv_installation/iptvrecorder19.jpeg)

A la fin de l'enregistrement, vous pouvez le retrouver à cet emplacement "**special://temp**" ou via l'extension IPTV Recoder. Vous pouvez ajouter ce répertoire dans les sources vidéo de Kodi.

![](/img/live_tv_installation/iptvrecorder20.jpeg)

![](/img/live_tv_installation/iptvrecorder21.jpeg)

![](/img/live_tv_installation/iptvrecorder22.jpeg)