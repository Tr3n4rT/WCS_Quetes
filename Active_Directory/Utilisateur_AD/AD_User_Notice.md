# Utilisation de l'Active Directory

## Rejoindre un Active Directory avec powershell
Dans une console powershell de la machine cliente, entrer la commande :
```powershell
Add-Computer -DomaineName "wilder.lan" -restart
```

Une fenêtre s'affiche afin de nous connecter avec les idientifiantes d'un utilisateur de l'active directory (nous pouvons utiliser les identifiants administrateur du serveur si aucun utilisateur n'a encore été enregistré)

## Ouvrir une session windows avec son compte utilisateur 
Pour se connecter à sa session windows, à l'écran de connexion, l'utiliteur est invité à saisir son identifiant de connexion et son mot de passe. L'identifiant de connexion utilisateur est composé de la première lettre de son prénom, d'un point, suivi de son nom de famille. Le tout sans espace. 
(Pour l'administrateur, il s'agit du nom de l'utilisateur entré dans la base de donnée SAM). 
Exemples de login :

- Jean Dupond 
  - j.dupond
- Jean Marc Morendini Serpentar
  - jm.morendiniserpentar


