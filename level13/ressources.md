## 1. Analyser l'executable level13

    UID 2013 started us but we we expect 4242

À part le problème de l'UID incorrect, nous ne pouvons pas vraiment intervenir, car nous n'avons pas les droits sudo pour modifier l'utilisateur.

## 2. Exporter le fichier par scp puis l'analyser avec Ghidra dans dogbolt

  uVar2 = ft_des("boe]!ai0FB@.:|L6l@A?>qJ}I");
  printf("your token is %s\n",uVar2);

À la fin du main, on constate que le token est ft_des("boe]!ai0FB@.:|L6l@A?>qJ}I"). Nous allons donc reprendre cette fonction et l'exécuter en local pour observer le résultat.

    Cela affiche: 2A31L79asukciNyi8uppkEuSx

## 3. Connexion

su level14

    Mot de passe : 2A31L79asukciNyi8uppkEuSx