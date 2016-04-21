# Utilisation de git avec github
## Cloner la branche master
`git clone https://... dossier cd dossier`

## Récupérer une branche qui est sur le serveur
### Avec les mêmes noms en local et sur le serveur (plus simple) ###
`git checkout brancheDistante`

### Avec des noms différents (plus compliqué mais plus personnalisable):
`git checkout -b brancheLocale` pour créer la branche localement.   
Puis `git branch --set-upstream-to=origin/brancheDistante brancheLocale` pour récupérer la branche distante depuis Github et la lier à la branche locale.

## Envoyer une branche locale sur le serveur
`git push --set-upstream origin brancheLocale`

## Supprimer une branche
Localement : `git branch -d brancheLocale`   
Sur le serveur : `git push origin --delete brancheDistante`

## Changer de branche localement
`git checkout brancheLocale`

## Récupérer les nouveautés depuis le serveur
`git pull`

## Ajouter un nouveau fichier à commiter
`git add fichier`

## Annuler l'ajout d'un fichier
`git reset HEAD -- fichier`


## Enregistrer les modifications sur la branche locale
`git commit fichierA fichierB ...`  
Tout d'un coup: `git commit -a`

## Appliquer les commit locaux sur le serveur
`git push`

## Voir les changements des fichiers locaux par rapport au dernier commit
`git status`

## Annuler un commit local
### Méthode soft (seul le commit et retiré, les fichiers restent tels quels):
Dernier commit : `git reset HEAD`  
Avant-dernier commit : `git reset HEAD^`  
Avant-avant-dernier : `git reset HEAD~2 `  
Commit numéro x : `git reset numeroDuCommit` (pas besoin de mettre tout le numéro, juste les 4-5 premiers chiffres)

### Méthode hard (le commit et retiré et les changements annulés): Même chose mais avec l'option --hard:
`git reset --hard HEAD`  
`git reset --hard HEAD^`  
`git reset --hard HEAD~2`  
`git reset --hard numeroDuCommit`

## Voir la liste des commits locaux
`git log`

## Restaurer un fichier comme il était au dernier commit
`git checkout fichier`
