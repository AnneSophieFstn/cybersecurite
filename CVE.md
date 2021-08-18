# Common Vulnerabilities and Exposures (CVE)

C'est un dictionnaire des informations publiques relatives aux vulnérabilité de sécurité.
Le dictionnaire est maintenu par l'organisme MITRE, soutenu par le département de la Sécurité intérieure des États-Unis.


# Présentation CVE

La mission principale du programme CVE est d'identifié, définir, et de cataloguer publiquement les vulnérabilités de cybersécurité. Il existe un enregistrement CVE pour chaque catalogue de vulnérabilités. 
Les vulnérabilités sont découvert puis assignés et publié par des organisations venant de partout dans le monde et qui sont partenaire avec le "Programme CVE".

Les partenaires publie les enregistrements CVE afin de communiquer de pertinente descriptions des vulnérabilités.
Les professionnels de l'information technologique et de la cybersécurité utilisent les enregistrement CVE pour s'assurer qu'ils discutent du même problème et pour coordonner leurs efforts pour hiérarchiser et traiter les vulnérabilités.

Source: https://cve.mitre.org/index.html
 

## Exemple: HiveNightmare - CVE-2021-36934

Cette vulnérabilité affecte certains fichiers système, dont le **gestionnaire des comptes** de sécurité et permet d’**exécuter du code arbitraire** avec les **droits SYSTEM** à partir d’un **compte utilisateur standard** : 

 - Un **utilisateur non-administrateur et malveillant** peut donc, en
   cas d’accès à une machine vulnérable, **obtenir des privilèges** plus
   **élevés**.

## Comment se protéger ?


Microsoft a publié une solution de contournement sur son site Web pour protéger les appareils contre les exploits potentiels.

Les administrateurs peuvent activer l'héritage ACL pour les fichiers dans %windir%system32config selon Microsoft.

   1. Sélectionnez Démarrer
    2.  Tapez cmd.
    3.  Sélectionnez Exécuter en tant qu'administrateur.
    4.  Confirmez l'invite UAC.
    5.  Exécutez icacls %windir%system32config*.* /inheritance:e
    6.  vssadmin delete shadows /for=c: /Quiet
    7.  vssadmin list shadows

La commande 5 active l'héritage ACL. 
La commande 6 supprime les clichés instantanés existants et la commande 7 vérifie que tous les clichés instantanés ont été supprimés.
