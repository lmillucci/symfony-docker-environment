# Symfony environment
Questo repository contiene la configurazione Docker necessaria a creare una nuova applicazione [Symfony](https://symfony.com/) tramite la Symfony CLI.
Per ulteriori informazioni puoi anche visitare il post che ho scritto sul [mio blog](https://www.lorenzomillucci.it/)

# Setup
- Crea i container con il comando:
`docker-compose up -d --build`

- connettiti al container con:
`docker exec -it symfony-environment bash`

- per evitare errori con la CLI di Symfony configura git con i comandi:
```
git config --global user.email "you@example.com"
git config --global user.name "Your Name" 
```

- crea un nuovo progetto con il comando:
`symfony new --full *NOME_PROGETTO*`

- Spostati all'interno della cartella del progetto e avvia il server con il comando: 
```
cd *NOME_PROGETTO*
symfony serve
```

- Collegati con il browser a `localhost:80`