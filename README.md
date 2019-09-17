# Merge from Master to Round Branch
How to incorporate changes made to the master templates into .do files being used for data collection (_Français ci-dessous_)

_Video:_ [Merge from Master to Branch](https://www.youtube.com/watch?v=7IMduSaKedY&list=PLaCCIQf3NY979c70cnegKx8Cmo3Wltkia&index=13&t=0s)

### Summary 
Merging from the master to the round is similar to submitting a pull request, however it is automatic, meaning that approvals do not need to occur. Merging is used to take changes that were made to the .do files during data collection (made in a .do file editing branch, and then integrated into the master branch via a pull request) and integrate them into the round branch. By merging, you are able to integrate the changes, without losing any of the country-specific updates (macros, languages, etc.) that are necessary to run the .do files during data collection.

#### By the end of this video, you should be able to:
- Initiate a merge from the master to a branch
- Address merge conflicts using the merge conflicts pane
- Accept correct version of conflicts


### How Tos
#### How to merge from the master branch to a round branch:
1. Make sure that you’re in the ROUND branch
2. Right click, or control click, on the master branch in the commit graph, and select “merge master into round 7” from the menu
    - Possible result 1 – “Merge Successful”: The merge was successful, and work can continue
    - Possible results 2 – “Merge Failed”: Need to resolve merge conflicts (below)
    
#### How to resolve a merge conflict:
A merge conflict occurs when the same line of code was edited differently in two branches. You will know there are merge conflicts because GitKraken will say display a note saying “Merge failed, there are merge conflicts that need to be resolved”. To resolve a merge conflict, do the following:
1. In the commit panel, there will be a note saying “X file conflict in the working directory” where X is a number (1, 2, 3, etc.)
2. Click “View Conflict”
3. GitKraken will now display the “conflicted files” and the “resolved files”
    - Conflicted Files: Files with conflicting changes, need to tell GitKraken which file has the correct version of the change
    - Resolved Files: Do not need to address a conflict
4. Click on “Conflicted File”
5. GitKraken will display a screen similar to the diff viewer
    - Left side: what the .do file looks like in the round branch (branch being merged into)
    - Right side: what the .do file looks like in the master branch (branch the merge is coming from)
6. Select the correct versions of each conflicted change by clicking on the check mark next to the correct change
    - Go to the commit graph and review the commits related to the conflicted changes to determine which is the correct version
    - If it is a country-specific change (macros, languages, etc.) keep the change from the round
7. Review the finalized .do file in the output pane
8. Click “Save” in the top right corner
9. Files will move into the “Staged files”
10. Click the button that says “commit and merge”
11. Push the round branch to GitHub


### Glossary of terms:
| Term | Definition |
| ---- | ---------- |
| Branch | A branch is a parallel version of a repository that allows you to work freely without disrupting the master version of a file. PMA uses branches to update .do file content and prepare .do files for round specific data collection |
| Commit | A commit is a way to save a change to a file that also stores information on what changes were made, when and by who. PMA uses commits to systematically document changes to .do files |
| Fork | A fork is a copy of a repository that lives in a separate account or organization. Forks allow changes to be made to a repository without affecting the original, while maintain a link between the two so that pull requests can be submitted between the two. PMA forks all repositories from the PMA_DM Organization to the Country Organizations, allowing for .do file updates to be shared across organizations |
| Master | The default branch that is made each time a new repository is created. At PMA, the master branch contains the template of any give .do file. No changes should be made in the master branch |
| Merge | Takes the changes from one branch and applies them into another branch, often via a pull request. PMA uses merges to share updates to the .do file templates |
| Push | Sending committed changes to a remote version of the repository. GitKraken pushes data to GitHub to keep the two platforms synced |
| Repository | Contains all of the project files and documentation and stores each file’s revision history. Can have multiple collaborators. PMA keeps its .do files in repositories that are organized by survey type and action |
| Staged File | Files manually added to the index that are ready to commit |
| Working Directory | Currently checked out version of the files in the local repository. It is the location on the computer where all repositories and .do files are stored |



_________________________________________________________________



# Merge du Master à une Branch de vague d’enquête
Comment incorporer les modifications des modèles master aux .do files utilisés pour la collecte des données

_Vidéo:_ [Merge du master à la branch vague](https://www.youtube.com/watch?v=u7uSfR-71-A&list=PLaCCIQf3NY97bYG9q4ha8mEUlM8W7kJpE&index=13&t=0s)


### Résumé  
Fusionner du master avec la branche de vague d’enquête ressemble à envoyer une pull request, cependant, il s’agit d’un processus automatique, en d’autres termes, aucune autorisation n’est nécessaire. La fonction « merge » est utilisée pour intégrer les modifications apportées aux .do files pendant la collecte des données (faites dans une branch d’édition des .do files, puis intégrées à la master branch via une pull request) dans une branch de vague d’enquête. En fusionnant les modifications, vous pouvez les intégrer sans perdre les mises à jour propres à votre pays (macros, langues, etc.), qui sont nécessaires pour exécuter les .do files pendant la collecte des données. 

#### A la fin de la vidéo, vous devriez être en mesure de :
- Initier un merge depuis la master vers une branch
- Résoudre les conflits merge en utilisant le panel de conflits merge 
- Accepter les versions exactes des modifications non concordantes


### Comment Faire
#### Comment fusionner (merge) de la master branch à une branch de vague d’enquête :
1. Assurez-vous de vous trouver dans la branch de votre VAGUE
2. Cliquez-droit, ou cliquez contrôle, sur la master branch dans le graphique des commits, puis sélectionnez “merge master into round 7” dans le menu
    - Résultat possible 1 – “Merge Successful”: La fusion (merge) a réussi, le travail peut continuer.
    - Résultat possible 2 – “Merge Failed”: La fusion (merge) a échoué, les conflits de fusion doivent être résolus (ci-dessous).


### Comment résoudre un conflit merge :
Un conflit de fusion (merge) a lieu lorsqu’une même ligne de code a été éditée différemment dans les deux branches. Vous saurez qu’il y a des conflits de ce type lorsque GitKraken affichera un message indiquant : “Merge failed, there are merge conflicts that need to be resolved” (« La fusion a échoué, il y a des conflits merge à résoudre »). Pour résoudre un conflit merge, suivez les étapes suivantes :
1. Dans le panel du commit, vous verrez un message indiquant : “X file conflict in the working directory” (« X conflits de fichier dans le working directory »), « X » étant un nombre (1, 2, 3, etc.) 
2. Cliquez sur “View Conflict” (Voir le conflit)
3. GitKraken affichera à présent les fichiers en conflit (“conflicted files”) et ceux résolus (“resolved files”)
    - « Conflicted Files » : Fichiers comportant des modifications non concordantes ; vous devrez indiquer à GitKraken quel fichier est la bonne version de la modification.
    - « Resolved Files » : Pas de conflit à résoudre
4. Cliquez sur “Conflicted File” (Fichier en conflit)
5. GitKraken affichera un écran similaire à la lecture diff 
    - À gauche : ce à quoi ressemble le .do file dans la branch de la vague (branch dans laquelle sont fusionnées les modifications)
    - À droite : ce à quoi ressemble le .do file dans la master branch (branch d’où provient le merge)
6. Sélectionnez les bonnes versions de chaque modification non concordante en cliquant dans la case à côté de la modification exacte.
    - Allez dans le graphique du commit et examiner les commits liés aux modifications conflictuelles pour savoir quelle est la bonne version.
    - S’il s’agit d’une modification propre à un pays en particulier (macros, langues, etc.), gardez la modification de la vague.
7. Examinez le .do file final dans le panel des outputs 
8. Cliquez sur “Save” (Sauvegarder) en haut à droite
9. Les fichiers seront déplacés sous “Staged files”
10.	Cliquez sur le bouton “commit et merge”
11.	Push la branch de la vague sur GitHub


### Glossaire :
| Terme | Definition |
| ---- | ---------- |
| Branch | Version parallèle d’un repository permettant de travailler librement sans perturber la version master d’un fichier. PMA utilise des branches pour mettre à jour le contenu des dofiles et les préparer pour la collecte de données d’une vague d’enquête spécifique. |
| Commit | Manière de sauvegarder une modification d’un fichier en stockant aussi des informations sur les changements qui ont été faits, quand et par qui. PMA utilise des commits pour documenter systématiquement les modifications des .do files |
| Master | Branch par défaut générée à chaque fois qu’un nouveau repository est créé. À PMA, la master branch contient le modèle de chaque .do file. Aucune modification ne devrait être apportée à la master branch |
| Merge | Applique les modifications d’une branch à une autre branch, souvent via une pull request. PMA utilise la fonction merge pour partager des mises à jour de modèles de .do files |
| Push | Envoyer des modifications d’un commit vers une version remote (à distance) d’un repository. GitKraken push (pousse) les données sur GitHub pour que les deux plateformes soient synchronisées. |
| Repository | Contient tous les fichiers et la documentation du projet, et stocke l’historique de révision de chaque fichier. Peut avoir plusieurs collaborateurs. PMA garde ses .do files dans des repositories organisés par type d’enquête et d’action |
| Fichier Stagé | Fichiers manuellement ajoutés et prêts pour le commit.|
| Working Directory | Version actuellement « checked out » des fichiers dans le repository local. C’est l’endroit sur l’ordinateur où tous les repositories et les .do files sont stockés. |
