# VUE DNS EVENT

La vue personnalisée __DNS event__ filtre les sources d'événements liées au DNS coté serveur et coté client. Elle inclue spécifiquement les événements :
- D'echec de la classe MSFT_NetLbfoTeamNic (ID 2)
- Des clients qui n'ont pas pu accéder à une ressource du serveur (ID 4)
- Les clé n'ayant pas pu être décryptés (ID 409)
- La zone %1 est manquante ou est corompue dans les données de registre (ID 501)
- Le service DNS n'est pas pu démaré ou une ressource système n'est pas accessible (ID 6001)

Elle exclue les événements de type :

- Problème de redirection d'un dossier (ID -502)
- Les abqndons de transfert de Zone par le serveur DNS (ID -6002)
