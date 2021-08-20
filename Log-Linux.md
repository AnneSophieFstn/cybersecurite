# Fichiers Logs sur Linux
Un **log** se présente sous la forme d'un fichier texte classique, reprenant de façon chronologique, l'ensemble des événements qui ont affecté un système informatique (logiciel, application, serveur, etc...) et l'ensemble des actions qui ont résulté de ces événements.

## Leurs emplacements

Les fichiers avec les logs sont sous **/var/log**

## Les différents Log et leur rôles sur linux ? 

| Emplacement |  Contenu|
|--|--|
|/var/log/alternatives.log | Les logs d'update-alternatives. |
|/var/log/apache2/* | Les logs du serveur http apache2. |
|/var/log/apt/*|  Les logs d'apt. Tous les paquets installés avec apt-get install, par exemple.|
|  /var/log/aptitude| Les logs d'aptitude. Contient toutes les actions demandées, même les abandonnées. |
|  /var/log/auth.log| Les informations d'autorisation de système. Y sont consignées toutes les connexions (réussies ou pas) et la méthode d'authentification utilisée. |
| /var/log/bind.log | Les logs du serveur de nom bind9, s'il sont activés. |
| /var/log/boot.log | Les informations enregistrées lors du démarrage du système. Ce fichier n'est pas activé par défaut. |
|/var/log/btmp  | Semblable à /var/log/wtmp. Affiche les connexions/déconnexions au système # lastb alors que # last lira le fichier /var/log/wtmp. |
|/var/log/cups/*  | Les logs du système d'impression cups. |
|/var/log/cron  | Les informations sur les tâches cron. Enregistrement à chaque fois que le démon cron (ou anacron) commence une tâche. |
| /var/log/daemon.log | Les informations enregistrées par les différents daemons (processus) de fond qui fonctionnent sur le système. |
| /var/log/debug | Les logs de debugging. |
| /var/log/dmesg | Les messages du noyau Linux depuis le démarrage. |
| /var/log/dpkg.log | Les informations sur les paquets installés ou retirés en utilisant la commande dpkg. |
| /var/log/fail2ban.log | Les Ban/Unban et infos sur le programme (Error, Info, etc.) si fail2ban est installé. |
| /var/log/faillog | Les échecs de connexion. # faillog -u root. |
| /var/log/kern.log | Les informations enregistrées par le noyau. Utile pour débogguer un noyau personnalisé, par exemple. |
| /var/log/lastlog | Les informations de connexion récente de tous les utilisateurs. Ce n'est pas un fichier ascii. Vous devez utiliser la commande lastlog pour afficher le contenu de ce fichier. |
| /var/log/mail.* | Les informations du serveur de messagerie. Par exemple, sendmail enregistre des informations sur tous les éléments envoyés dans ces fichiers. |
| /var/log/messages | Les messages du système, y compris les messages qui sont enregistrés au démarrage. Beaucoup de choses sont enregistrées dans /var/log/ messages y compris le courrier, cron, daemon, kern, auth, etc. |
| /var/log/syslog | Tous les messages, hormis les connexions des utilisateurs. Plus complet que /var/log/messages. |
| /var/log/user.log | Les informations sur tous les journaux de niveau utilisateur. |
| /var/log/wtmp | Toutes les connexions et déconnexions: last -f /var/log/wtmp. |
|/var/log/Xorg.x.log  |  Les messages du serveur X. N'existe pas sur un serveur. Le petit x est le N° d'instance du serveur X.|

## Chercher au moins 1 trace de vos attaques grâce aux logs concernant l'activité 'blog'.

Une fois dans le Shell on exécute la commande:

    find / -type f -name *.log

Cette commande va nous permettre de trouver l'ensemble des fichiers `.log`

Ce qui va nous intéresser parmi la liste des fichiers log donner ce sera:

    apache2/access.log

A l'intérieur de ce fichier on retrouve les traces de nos attaques.
