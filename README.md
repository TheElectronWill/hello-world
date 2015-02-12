# Utilisation de git avec github
<center><b>Cloner la branche master:</b></center><br>
<code>git clone https://... dossier
cd dossier</code>

<center><b>Récupérer une branche qui est sur le serveur:</b></center>
<p>Avec les mêmes noms en local et sur le serveur (plus simple):<br>
<code>git checkout brancheDistante</code>
</p>
<p>
Avec des noms différents (plus compliqué mais plus personnalisable):<br>
<code>git checkout -b brancheLocale #Pour créer la branche localement.</code><br>
Pour récupérer la brancheDistante depuis Github et la lier à la brancheLocale:<br>
<code>git branch --set-upstream-to=origin/brancheDistante brancheLocale</code> 
</p>

<center><b>Envoyer une branche locale sur le serveur:</b></center>
<p>
<code>git push --set-upstream origin brancheLocale</locale>
</p>

<center><b>Supprimer une branche</b></center>
<p>
Localement: <code>git branch -d brancheLocale</code><br>
Sur le serveur: <code>git push origin --delete brancheDistante</code>
</p>

<center><b>Changer de branche localement</b></center>
<p>
Localement: <code>git checkout brancheLocale</code>
</p>

<center><b>Récupérer les nouveautés depuis le serveur</b></center>
<p>
<code>git pull</code>
</p>

<center><b>Ajouter un nouveau fichire à commiter</b></center>
<p>
<code>git add fichier</code>
</p>

<center><b>Annuler l'ajout d'un fichier</b></center>
<p>
<code>git reset HEAD -- fichier</code>
</p>

<center><b>Enregistrer les modifications sur la branche locale</b></center>
<p>
<code>git commit fichierA fichierB ...</code><br>
Tout d'un coup: <code>git commit -a</code>
</p>

<center><b>Appliquer les commit locaux sur le serveur</b></center>
<p>
<code>git push</code>
</p>

<center><b>Voir les changements des fichiers locaux par rapport au dernier commit</b></center>
<p>
<code>git status</code>
</p>

<center><b>Annuler un commit local</b></center>
Méthode soft (seul le commit et retiré, les fichiers restent tels quels):
<p>
Dernier commit:<code>git reset HEAD #Dernier commit</code><br>
Avant-dernier commit:<code>git reset HEAD^</code><br>
Avant-avant-dernier:<code>git reset HEAD~2 </code><br>
Commit numéro x:<code>git reset numeroDuCommit</code> (pas besoin de mettre tout le numéro, juste les 4-5 premiers chiffres)
</p>
Méthode hard (le commit et retiré et les changements annulés): Même chose mais avec l'option --hard:
<p>
<code>git reset --hard HEAD</code><br>
<code>git reset --hard HEAD^</code><br>
<code>git reset --hard HEAD~2</code><br>
<code>git reset --hard numeroDuCommit</code>
</p>

<center><b>Voir la liste des commits locaux</b></center>
<p>
<code>git log</code>
</p>

<center><b>Faire redevenir un fichier comme il était au dernier commit</b></center>
<p>
<code>git checkout fichier</code>
</p>
