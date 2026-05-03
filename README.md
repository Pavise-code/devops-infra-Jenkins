Voici les différentes ressources et commandes dans le projet Jenkis
GitHub: 

## 📂 Repository:

Code de l'application (fil-rouge): https://github.com/Pavise-code/Jenkin-project-red-thread.git

l'infrastructure de Jenkins (enfra-Jenkins): https://github.com/Pavise-code/devops-infra-Jenkins.git



## Commande:

Commande pour mettre en place l'infrastructure de Jenkins (JenkinsBuild-infra-Jenkins) :
```console
docker-compose -f docker-compose-infra.yml up -d --build
```

Commande pour supprimer tous les conteneurs, images et volumes: 
```console
docker rm -f $(docker ps -aq) ; docker volume rm $(docker volume ls -q)
```


## App:

Commande a mettre dans powershell pour ajouter la base de donnée si dans l'application les options saisie-cotisation et liste-cotisation ne s'affiche pas:
```console
 Get-Content ./db/espacemembre.sql | docker exec -i cotisations\_db mysql -u root -prootpass EspaceMembreDB
```







