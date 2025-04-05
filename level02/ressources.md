## 1. Récupérer le fichier .pcap avec scp

    scp -P 4242 level02@192.168.56.101:/home/user/level02/level02.pcap .

Changer les permissions

    chmod 777 level02.pcap

## 2. Ouvrir et analyser le fichier .pcap dans Wireshark

Utilisez l'option "Follow TCP Stream" pour suivre un flux spécifique.

    Cela affiche: Password: ft_wandr...NDRel.L0L

En observant les packets correspondant aux '.', on voit que le '.' correspond a 7F ce qui en code ASCII donne 'DEL'.

Donc en supprimant les caracteres avant les points on obtient : ft_waNDReL0L

## 3. Connexion

su flag02

    Mot de passe : ft_waNDReL0L
    Commande pour obtenir le flag : getflag
    Résultat : kooda2puivaav1idi4f57q8iq

su level02

    Mot de passe : kooda2puivaav1idi4f57q8iq