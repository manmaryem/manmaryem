# Installation de Wireshark et analyse de trames ethernet #
##### Les questions ##### 

1. ### Quels protocoles ont été utilisés dans la trace réseau capturée ? ###
_La colonne 5 Protocole : c'est le type du paquet. ici il s'agit du protocole ARP et ICMP_
- ICMP (Internet Control Message Protocol) est un protocole de communication utilisé dans les réseaux IP (Internet Protocol). il aide à identifier les problèmes de connectivité, à diagnostiquer les erreurs de communication et à mieux comprendre le comportement du réseau en fournissant des informations sur les messages ICMP échangés entre les appareils réseau.
- ARP Le protocole ARP (Address Resolution Protocol). il résoud les adresses IP en adresses MAC dans les réseaux locaux Ethernet. Wireshark affiche les adresses IP source et destination dans les messages ARP, ainsi que les adresses MAC source et destination associées. Cela permet de voir les correspondances entre les adresses IP et les adresses MAC pour les appareils communiquant sur le réseau local.  
#### j'ai eu cette information en allant directement sur le site de wireshark afin de comprendre ses fonctionalités ####
2. ### Quelles sont les adresses IP et les adresses MAC des interfaces ayant échangé des informations ? ###
  - l'adresse MAC est dans "Source"et "Destination" de l'en-tête Ethernet ![image](https://github.com/manmaryem/manmaryem/assets/137881827/83a658da-c739-4f9a-bf12-e2d968400425)
  - les adresses IP sont en l'en-tête IP du paquet, on les trouveres dans les champs "Source"vet "Destination" de l'en-tête IP. ![image](https://github.com/manmaryem/manmaryem/assets/137881827/641e74b6-256f-4ed5-add5-e64d3f845173)

3. ### Quel filtre d'affichage permet de ne plus afficher les paquets ARP ? ###
   la barre du filtre d'affichage  ![image](https://github.com/manmaryem/manmaryem/assets/137881827/5ed96ca1-a91f-43bb-8cef-f22ad275f101)


4. ### Quelles informations sont disponibles dans la colonne info de la liste des paquets pour la ligne 3 ? ###
   
 -   ![image](https://github.com/manmaryem/manmaryem/assets/137881827/85e7d5df-afa0-4a74-b25c-aed78498033c)

   - Un "ping request" (demande de ping), il est utilisé pour envoyer une requête de ping depuis un appareil source vers un appareil de destination.
Lorsqu’une commande ping est exécuté depuis un appareil source vers un appareil de destination, l'appareil source envoie des paquets ICMP Echo Request. Le paquet ICMP Echo Request contient des informations telles que l'adresse IP source et l'adresse IP de destination. Il est utilisé pour tester la connectivité entre les deux appareils. L’appareil de destination reçoit une demande de ping, il doit répondre avec un paquet ICMP Echo Reply pour indiquer qu'il est disponible et pour fournir le temps de réponse.

     
6. ### Le paquet N°8 est-il une question ou une réponse ? ###
*et quel est le paquet correspondant (la question, si c'est une réponse ou la réponse, si c'est une question ?*
![image](https://github.com/manmaryem/manmaryem/assets/137881827/3bf3f284-53be-42da-a628-9806cc71db90)

- Un "ping reply" (réponse de ping) en réponse à un paquet ICMP Echo Request donc ici il s'agit de la réponse pour le paquet 7 (demande d'écho) lorsqu'un appareil est "pingé".
Lorsqu’une commande ping est exécuté depuis un appareil source vers un appareil de destination, l'appareil source envoie des paquets ICMP Echo Request à l'appareil de destination. Si l'appareil de destination est accessible et fonctionnel, il répondra avec des paquets ICMP Echo Reply. 



