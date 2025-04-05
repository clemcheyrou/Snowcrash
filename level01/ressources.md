## 1. Rechercher l'utilisateur flag01 dans le fichier /etc/passwd

grep flag01 /etc/passwd

    Cela affiche : 42hDRfypTqqnw

## 2. Utilise de John the Ripper sur une VM

John est l'un des logiciels de cassage de mots de passe les plus populaires, car il inclut l'autodétection des fonctions de hachage utilisées pour stocker les mots de passe.

On recupere le fichier en local

    scp -P 4242 level01@192.168.56.101:/etc/passwd .

    ./john passwd

    Cela affiche: abcdefg

## 2. Connexion

su flag01

    Mot de passe : abcdefg
    Commande pour obtenir le flag : getflag
    Résultat : f2av5il02puano7naaf6adaaf

su level01

    Mot de passe : f2av5il02puano7naaf6adaaf