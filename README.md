PROCEDURE:  /
____________/

-Installer une machine virtuelle Xubuntu (lien:  http://cdimage.ubuntu.com/xubuntu/releases/trusty/release/)

- Créer un nouveau fichier .vdi via VirtualBox, et choisir le fichier .iso téléchargé sur le lien vi-dessus comme périphérique de démarrage

-Suivre la procédure d'installation

-Pour installer les différents programmes, entrer la commande dans le terminal:

		sudo apt-get install mysql-server
		sudo apt-get install apache2
		sudo apt-get install ruby
		sudo apt-get install jekyll
		sudo apt-get install git

- Créer le répertoire "site" dans le dossier personnel de la machine virtuelle et sur github

- Entrer la commande dans le terminal: git clone https://github.com/"votre pseudo"/site.git

- Pour générer une clé ssh: ssh-keygen -t ras -C "nicolas.arribard@gmail.com" et choisir nom du fichier et extension.

- La clé ssh est désormais dans le fichier "site"

- Sur le compte github aller dans "setting/SSH keys" et cliquer sur "genette SSH key"

- Choisir le nom et entrer la clé SSH reçue dans le répertoire site

- Sur la machine virtuelle aller dans etc/apache2/apache2.conf et faire un ledit pour rajouter les droits sur le dossier /home/xubuntu/site

- Aller dans sites-available et modifier le fichier 000-default.conf avec gedit pour DocumentRoot et mettre /home/xubuntu/site/site

- Executer la commande "service apache2 restart" 

- Dans le navigateur, aller a "127.0.0.1" Et vérifier si le fichier "README" est bien visible
