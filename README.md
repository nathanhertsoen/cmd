# cmd

Supprimer tout ce que contient le cache du serveur apache (sans supprimer le cache grÃ¢ce Ã  *)
rm -rf /var/www/html/[nom du projet]/writable/cache/*

Supprimer un dossier et tous ses sous-dossiers et fichiers
rm -rf [nom du dossier]/

CrÃ©er un dossier codeigniter4 dans /var/www/html
composer create-project codeigniter4/appstarter project-root

Fichier pour changer le repertoir de projet d'apache (un mauvais rÃ©pertoir peut causer une erreur 404)
/etc/apache2/sites-available/000

Afficher tous les processus en cours
ps -aux

Afficher tous les processus en cours (version plus recente)
htop
(sudo apt install htop, si Ã§a ne fonctionne pas)

Visualiser un projet php sur un port au choix sans lancer de serveur apache 
php -S adress:port
Exemple : 
(On se place dans le repertoir qui contient l'index du projet) --> /var/www/[monProjet]/public
(On choisi l'adresse et le port qu'on veut)                    --> php -S localhost:port

Tuer une fenetre au clic
xkill

Tuer un processus avec son id (voir htop ou ps -aux)
kill pid

Relancer le PC
sudo reboot

Trouver son fichier php.ini
php -i | grep "Loaded Configuration File"
(Sinon c'est lÃ  ====>) /etc/php/7.2/apache2/php.ini

Observer les logs apache
tail -f /var/log/apache2/*.log

afficher tous les fichiers 
ls -l

afficher tous les fichiers (mÃªme cachÃ©s)
ls -al

afficher tous les fichiers mÃªme cachÃ©s (avec leur poids de maniÃ¨re plus lisible)
ls -alh

Rechercher un paquet
sudo apt-cache search [nom d'un paquet]

Lister des rÃ©sultats par mot clef
[commande] | grep [mot clef]
Exemple : ls -al | grep index

Changer les droits d'un fichier
chmod
Exemple : https://doc.ubuntu-fr.org/permissions#en_ligne_de_commande1

Changer le propriÃ©taire d'un dossier et de ses sous-dossiers
chown [nom]:[nom] .
Exemple (une fois dans le dossier concernÃ©) : 

-> cd [dossierparent/bondossier]
-> chown -R nathan:nathan [nom du dossier]

gÃ©rer apache2
sudo /etc/init.d/apache2 status
sudo /etc/init.d/apache2 stop
sudo /etc/init.d/apache2 start
sudo service apache2 restart
sudo service apache2 reload



|-----------------------------------------------------------------------------------------------------|
|                          Correspondances de representation des droits                               |
|-----------------------------------------------------------------------------------------------------|
|          Droit           |   Valeur alphanumerique    |   Valeur octale   |   Valeur binaire        |
|--------------------------|----------------------------|-------------------|-------------------------|
|   Aucun droit            |          ---               |        0          |    000                  |   
|--------------------------|----------------------------|-------------------|-------------------------|
|   Execution seulement    |          --x               |        1          |    001                  |
|--------------------------|----------------------------|-------------------|-------------------------|   
|   ecriture seulement     |          -w-               |        2          |    010                  |
|--------------------------|----------------------------|-------------------|-------------------------|
|   ecriture et execution  |          -wx               |        3          |    011                  |
|--------------------------|----------------------------|-------------------|-------------------------|
|   Lecture seulement      |          r--               |        4          |    100                  |
|--------------------------|----------------------------|-------------------|-------------------------|
|   Lecture et execution   |          r-x               |        5          |    101                  |
|--------------------------|----------------------------|-------------------|-------------------------|
|   lecture et ecriture    |          rw-               |        6          |    110                  |
|--------------------------|----------------------------|-------------------|-------------------------|
|   Tous les droits (rwx)  |          rwx               |        7          |    111                  |
|-----------------------------------------------------------------------------------------------------|
