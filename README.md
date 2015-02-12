# Utilisation de git avec github
<center><b>Cloner la branche master:</b></center><br>
<code>git clone https://... dossier
cd dossier</code>

<center><b>Récupérer une branche qui est sur le serveur:</b></center>
<p>
<code>git checkout -b brancheLocale #Pour créer la branche localement.
<code>git branch --set-upstream-to=origin/brancheDistante brancheLocale #Pour récupérer la brancheDistante depuis Github et la lier à la brancheLocale</code>
</p>

<center><b>Envoyer une branche locale sur le serveur:</b></center>
<p>
<code>git push --set-upstream origin brancheLocale</locale>
<p>

<center><b>Supprimer une branche</b></center>
<p>
Localement: <code>git branch -d brancheLocale</code>
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
<code>git commit fichierA fichierB ...</code>
Tout d'un coup: <code>git commit -a</code>
</p>

<center><b>Annuler un commit local</b></center>
Méthode soft (seul le commit et retiré, les fichiers restent tels quels):
<p>
<code>git reset HEAD #Dernier commit</code>
<code>git reset HEAD^ #Avant-dernier commit</code>
<code>git reset HEAD~2 #Avant-avant-dernier commit</code>
<code>git reset numeroDuCommit #Commit n°... (pas besoin de mettre tout le numéro, juste les 4-5 premiers chiffres)</code>
</p>
Méthode hard (le commit et retiré et les changements annulés):
<p>
<code>git reset --hard HEAD #Dernier commit</code>
<code>git reset --hard HEAD^ #Avant-dernier commit</code>
<code>git reset --hard HEAD~2 #Avant-avant-dernier commit</code>
<code>git reset --hard numeroDuCommit #Commit n°... (pas besoin de mettre tout le numéro, juste les 4-5 premiers chiffres)</code>
</p>

<center><b>Voir la liste des commits locaux</b></center>
<p>
<code>git log</code>
</p>

<center><b>Voir les changements par rapport au dernier commit local</b></center>
<p>
<code>git status</code>
</p>

<center><b>Faire redevenir un fichier comme il était au dernier commit</b></center>
<p>
<code>git checkout fichier</code>
</p>
