# MajDiscord
Permet de mettre à jour Discord de manière semi-automatique. Il suffit de télécharger la nouvelle version, il s'occupe du reste.

## Prérequis
<pre><code>apt install inotify-tools -y</code></pre>

Modifier le fichier `/etc/sudoers` et ajouter :
<pre><code>username ALL=(ALL) NOPASSWD: /usr/bin/dpkg -i /path/app</code></pre>

*Note : C'est pour avoir les notifications, pour ne pas avoir à ajouter un utilisateur en sudoer, il suffi de changer*
<pre><code>sudo dpkg -i "$directory"/"$new_file" > /dev/null 2>&1</code></pre>
*Par*
<pre><code>dpkg -i "$directory"/"$new_file" > /dev/null 2>&1</code></pre>
*Mais les notifications n'apparaîtrons pas.*

## Installation
<pre><code>git clone https://github.com/IAidenI/MajDiscord</code></pre>

**Penser à changer dans le chemin d'accès à checker + changer les deux images avec leur bon chemin d'accès (les images se trouvent dans src)**

Pour qu'il se lance au démmarage sous gnome
<p align="center">
  <img src="./src/image/1.png"/>
</p>
<p align="center">
  <img src="./src/image/2.png"/>
</p>
<p align="center">
  <img src="./src/image/3.png"/>
</p>
