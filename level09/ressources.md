## 1. Analyser le fichier binaire level09

Il semble rajouter +1 a chaque caractere

## 2. Reverse cette logique sur le contenu du token

Importer le fichier token en avec scp, autoriser la lecture en chmod, puis executer ce script.

    #include <stdio.h>
    #include <stdlib.h>

    void decremente_caracteres(FILE *fichier) {
        int c;
        int i = 0;
        while ((c = fgetc(fichier)) != EOF) {
            c -= i;
            printf("%c", (char)c);
            i++;
        }
    }

    int main() {
        FILE *fichier = fopen("/home/ccheyrou/token", "r");

        if (fichier == NULL)
            return 1;
        decremente_caracteres(fichier);
        fclose(fichier);
        return 0;
    }

    Ca affiche: f3iji1ju5yuevaus41q1afiuq
## 3. Connexion

su flag09

    Mot de passe : f3iji1ju5yuevaus41q1afiuq
    Commande pour obtenir le flag : getflag
    Résultat : s5cAJpM8ev6XHw998pRWG728z

su level10

    Mot de passe : s5cAJpM8ev6XHw998pRWG728z