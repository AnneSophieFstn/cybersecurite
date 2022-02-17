  # EDR (Endpoint Detection and Response)

## C'est quoi un EDR ? 

EDR désigne un logiciel permettant de détecter les menaces présentes sur un poste de travail ou sur un serveur. Il définit une catégorie d’outils et de solutions qui mettent l’accent sur la détection d’activités suspectes directement sur les hôtes du système d'informations. Il est caractérisé par ses capacités de **détection**, d’**investigation** et enfin de **remédiation**.

## La différence entre un antivirus et EDR ?

L'EDR est proactif ce qui fait qu'il est beaucoup plus évolué qu'un antivirus qui lui est réactif, l'EDR s'appuie sur des algorithmes d'intelligence artificielle  lui donnant la faculté d'être auto-apprenant et ainsi d'évoluer.

## Comment fonctionne un antivirus ?
Un antivirus déclenche sa phase d’analyse au moment de la détonation d’un logiciel malveillant comme un malware ou un ransomware. Il utilise un registre contenant des souches connues de virus et va chercher une correspondance entre l’empreinte informatique du fichier suspect et les malwares connus dans le registre.
Si le malware analysé est inconnu des registres, il sera classé comme fichier légitime et l'antivirus devient donc obsolètes.

## Comment fonctionne l'EDR ?
L’analyse comportementale, et monitore les actions d’un terminal. Cela permet par exemple de mettre en lumière les attaques « _fileless_ » qui vont exécuter des commandes de _powershell_. Si l’utilisateur n’en n’utilise jamais, le simple fait d’en voir apparaître surtout encodée en base 64 permettra à l’EDR de prendre la décision de bloquer le programme qui est à l’origine de la commande et pas seulement ladite commande.

## Source

 - [Emajit](https://www.emajit.com/conseils-informatique-cybersecurite/qu-est-ce-qu-un-edr/)
   
 - [Orange cyberdefense](https://orangecyberdefense.com/fr/solutions/protection-des-mobiles-et-des-endpoints/endpoint-detection-and-response-pourquoi-ledr/)

