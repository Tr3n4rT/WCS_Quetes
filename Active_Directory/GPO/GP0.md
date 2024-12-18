# Groupe Policies

## Commande pour les GPO
Pour afficher la liste de toutes les commandes du module __Group Policy__ de PowerShell :

```powershell
Get-Command -Module GroupPolicy
```

Pour afficher les GPO d'un domaine :
```powershell
Get-GPO -Domain <domain> -All
#Chercher une GPO d'après son nom
Get-Gpo -All | Where-Object DisplayName -match "<nom_GPO>"
#Chercher une GPO d'après son id
Get-GPO -ID <id_gpo>
#Afficher tout les GPO Hérités pour une OU
Get-GPInheritance -Target "OU=<OU>,DC=<DC>,DC=<DC>"
```

## Créer une Gpo
Ressource pour trouver le chemin d'une clé de registre spécifique :
 - [admx.help](https://admx.help/)
 - [gpsearch](https://gpsearch.azurewebsites.net/#4695)

1. Créer un nom de pour la GPO
Commencer par créer une GPO avec un nom sans aucune configuration :
```powershell
New-GPO -Name "DesactivateControlPanel" -Comment "Désactive l'accès et l'utilisation du panneau de contrôle et des paramètres associés"
New-GPO -Name "<nom_GPO>" -Comment "<commantaire"

```
- L'option -Name peut être n'importe quel nom explicite pour nommé la GPO
- L'option -Comment permet de commenter ou une décrire la GPO

2. Configurer la GPO
```powershell
Set-GPRegistryValue -Name "DesactivateControlPanel" -key "HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer" -ValueName NoControlPanel -Type REG_DWORD -Value 0 
Set-GPRegistryValue -Name "<nom_GPO>" -key "<Registry_Hive>\<path_clé_de_registre>" -ValueName <Value_Name> -Type <Type> -Value <register_specific_Value> 

```

3. Lier la GPO à une Unité Organisationnelle / Domaine / ~~
```powershell
New-GPlink -Name "DesactivateControlPanel"
```
```powershell
New-GPlink -Name "<nom>" -Target "OU=<OU>,DC=<DC>,DC=<DC>"
```
 
Registry Hive	HKEY_CURRENT_USER
Value Name	NoControlPanel
Value Type	REG_DWORD
Enabled Value	1
Disabled Value	0

gpupdate

gpresulte