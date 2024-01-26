# MajDiscord
Permet de mettre à jour Discord de manière semi-automatique. Il suffit de télécharger la nouvelle version, il s'occupe du reste.

## Prérequis
<pre><code>apt install inotify-tools -y</code></pre>

Modifier au besoin le fichier `/etc/sudoers` et ajouter :
<pre><code>username ALL=(ALL) NOPASSWD: /usr/bin/dpkg -i /path/app</code></pre>

*Note : C'est pour avoir les notifications, pour ne pas avoir à ajouter un utilisateur en sudoer, il suffi de changer*
<pre><code>sudo dpkg -i "$directory"/"$new_file" > /dev/null 2>&1</code></pre>
*Par*
<pre><code>dpkg -i "$directory"/"$new_file" > /dev/null 2>&1</code></pre>
*Mais les notifications n'apparaîtrons pas.*

## Installation
<pre><code>git clone https://github.com/IAidenI/MajDiscord;chmod +x MajDiscord/maj_discord</code></pre>

**Penser à changer dans le chemin d'accès à du téléchargement des fichiers**

Pour qu'il se lance au démmarage sous gnome :
Il faut ajouter le script à la variable d'environement PATH, pour cela éditer le fichier .bashrc (pour les environement bash, .zshrc pour zsh par exemple, pour savoir echo $SHELL) :
<pre><code>cat >> export PATH=/chemin/vers/le/dossier/qui/contient/maj_discord:$PATH;source ~/.bashrc</code></pre>

<p align="center">
  <img src="./src/image/1.png"/>
</p>
<p align="center">
  <img src="./src/image/2.png"/>
</p>
<p align="center">
  <img src="./src/image/3.png"/>
</p>
