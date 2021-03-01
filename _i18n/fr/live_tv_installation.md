> ⚠️ Cette fonctionnalité est uniquement disponible sous Kodi Leia (18) et versions supérieures

# Sommaire

* [Introduction](#introduction)
* [I. Prérequis](#i-prérequis)
* [II. Installation de IPTV Manager](#ii-installation-de-iptv-manager)
* [III. Activation des chaînes](#iii-activation-des-chaînes)
* [IV. Enregistrement des directs TV](#iv-enregistrement-des-directs-tv)
    * [1. Prérequis et Limitations](#1-prérequis-et-limitations)
    * [2. Installation de IPTV Recorder](#2-installation-de-iptv-recorder)
    * [3. Configuration et utilisation de IPTV Recorder](#3-configuration-et-utilisation-de-iptv-recorder)

# Introduction

Depuis la version 0.2.30 du plugin il est possible d'accéder aux différents flux de TV en direct proposés dans Catch-up TV & More directement depuis la fonctionnalité "TV" de Kodi.
Cette fonctionnalité utilise le plugin IPTV Manager ainsi que le PVR IPTV Simple.

Cette fonctionnalité a plusieurs avantages (liste non exhaustive) :

* Profiter pleinement du guide TV géré par Kodi
* Organiser les différentes chaînes dans des groupes
* Un seul endroit pour regrouper les chaînes des autres PVR et plugin vidéos (TNT, Satellite, ...)

Un petit aperçu du résultat final une fois que vous aurez suivi ce tutoriel :

![](/img/live_tv_installation/intro1.jpeg)

![](/img/live_tv_installation/intro2.jpeg)

![](/img/live_tv_installation/intro3.jpeg)

![](/img/live_tv_installation/intro4.jpeg)


# I. Prérequis

Si vous ne l'avez pas encore fait, il est nécessaire de procéder à l'installation de Catch-up TV & More afin de profiter de cette fonctionnalité. Suivez simplement ce [tutoriel](https://catch-up-tv-and-more.github.io/fr/installation/) avant de continuer ici.

Certaines chaînes nécessitent d'avoir un compte utilisateur afin de profiter de leur service (c'est par exemple le cas de 6play).
Le première chose à faire est de créer le(s) compte(s) nécessaire(s) directement sur le(s) site(s) internet des chaînes concernées.
Enfin, il est faut renseigner vos couples identifiants/mots de passe dans les paramètres du plugin.

Ouvrez Catch-up TV & More.

![](/img/live_tv_installation/accounts1.jpeg)

Accédez aux paramètres du plugin en appuyant sur la flèche gauche de votre clavier ou télécommande.

![](/img/live_tv_installation/accounts2.jpeg)

Enfin, rendez-vous dans l'onglet "Comptes" et renseignez vos identifiants et mots de passe pour les chaînes désirées.
N'oubliez pas de valider avec le bouton "OK" afin de sauvegarder vos réglages.

![](/img/live_tv_installation/accounts3.jpeg)


# II. Installation de IPTV Manager

Il est d'abord nécessaire d'installer IPTV Manager.
Pour cela rendez-vous dans les paramètres de Catch-up TV & More dans la section "Intégration TV" et choisissez "Installer le plugin IPTV Manager".

![](/img/live_tv_installation/install_iptvmanager_0.jpeg)

![](/img/live_tv_installation/install_iptvmanager_1.jpeg)


# III. Activation des chaînes

Une fois IPTV Manager installé, retournez dans les paramètres de Catch-up TV & More afin de sélectionner les chaînes que vous souhaitez voir apparaître dans la section TV de Kodi.
Cela se passe dans la section "Intégration TV" en choisissant "Sélectionner les chaînes TV à activer".
N'oubliez pas de sauvegarder vos paramètres en cliquant sur les boutons "OK".

![](/img/live_tv_installation/select_channels_0.jpeg)

![](/img/live_tv_installation/select_channels_1.jpeg)


Si vos chaînes n'apparaissent toujours pas dans la section "TV" de Kodi vous pouvez effectuer les étapes suivantes dans les réglages d'IPTV Manager :

1. "IPTV Simple" --> "Configure IPTV Simple automatically..."
2. "Channels" --> "Refresh channels and guide now..."

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