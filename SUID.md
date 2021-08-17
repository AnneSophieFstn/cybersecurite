# SUID linux

C'est l'une des puissantes autorisations spéciales que l'on peut définir pour les exécutables et les répertoires sous Linux. Il permet d'**allouer temporairement à un utilisateur les droits** du propriétaire du fichier, durant son exécution. 

En effet, lorsqu'un programme est exécuté par un utilisateur, les tâches qu'il accomplira seront restreintes par ses propres droits, qui s'appliquent donc au programme. 

Lorsque le droit SUID est appliqué à un exécutable et qu'un utilisateur quelconque l'exécute, **le programme détiendra** alors **les droits du propriétaire du fichier** durant son exécution. 
Bien sûr, **un utilisateur ne peut jouir du droit SUID** que s'**il détient par ailleurs les droits d'exécution** du programme. 

Ce droit est utilisé lorsqu'une tâche, bien que légitime pour un utilisateur classique, nécessite des droits supplémentaires (généralement ceux de _root_).

## Notation

Son flag est la lettre s ou S qui vient remplacer le x du propriétaire. La majuscule ou la minuscule du 's' permet de connaitre l'état du flag x (droit d'exécution du propriétaire) qui est donc masqué par le droit SUID 's' ou 'S': C'est un s si le droit d'exécution du propriétaire est présent, ou un S sinon. Il se place donc comme ceci :

 ---s------  ou  ---S------

Un fichier avec les droits

 -rwxr-xr-x

auquel on ajoute le droit SUID aura donc la notation

 -rwsr-xr-x

## Valeur

Le droit SUID possède la valeur octale 4000.  
Exemple : - r w s r - x r - x correspond à 4755.

## Exemple d'utilisation
Le droit SUID est utilisé pour le programme  _mount_  (généralement localisé dans /bin) :

 -rwsr-xr-x  1 root bin 68804 /bin/mount

## Protection contre une attaque de type sushi

Sur Linux, des restrictions de droit ont été faites sur le **drapeau SUID** :

-   pour un fichier de script, l'exécution se fera sans tenir compte du drapeau SUID
-   Il semble de plus que si un utilisateur autre que le propriétaire modifie le fichier, alors le bit SUID est remis à 0.

Il n'est pas sûr que les versions d'Unix actuelles aient implémenté cette sécurité ; dans ce cas, cela ouvre la porte à une attaque qui est appelée sushi (_su shell_) : l'utilisateur  _root_  crée un fichier de  shell avec le bit SUID en laissant les droits en écriture à d'autres utilisateurs ; l'un d'eux pourra modifier le fichier et exécuter tout ce qu'il voudra avec les droits de root.
