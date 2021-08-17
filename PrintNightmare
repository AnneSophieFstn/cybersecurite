# PrintNightmare

C'est une vulnérabilité trouvé dans le spouleur d’impression de Windows.


# Que fait cette vulnérabilité ?

Les failles PrintNightmare peuvent être utilisées pour des élévations de privilèges ou des exécutions de code à distance.

## Qui a été attaquer ?

Principalement les entreprises.

## Comment il s'active ?

PrintNightmare s'active par un appel à la fonction RpcAddPrinterDriver. De base, elle permet d'ajouter des pilotes d'impression. Ici, elle ouvre la voie à l'injection d'une DLL vérolée.

Seul un utilisateur authentifié - ou, sur les contrôleurs de domaine, un utilisateur du domaine - peut invoquer la fonction. Microsoft a listé les groupes dans lesquels on est susceptible d'en trouver. Et recommande deux options : désactiver soit le spouleur, soit l'impression distante.
Dans tout les cas, les contrôleurs de domaine sont tous affectés, quelle que soit leur version de Windows.

## Depuis quand cette faille existes ?
Depuis début juin, sept failles ont été révélées, affectant toutes le spouleur d’impression (CVE-2021-1675, CVE-2021-34527, CVE-2021-34481, CVE-2021-36936, CVE-2021-36947, CVE-2021-34483, CVE-2021-36958).
Toutes les failles ont été patchées sauf la dernière, qui date du 11 août.
