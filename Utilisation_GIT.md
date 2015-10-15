**Sur serveur local**
- Créer un répertoire pour envoyer et recevoir les fichiers vers/de Github
- Aller dans le répertoire
- Initialiser le répertoire ``` $ git init ```
- Créer un lien avec le repository sur Github ``` $ git remote add nom_lien url_repository_github ``` Généralement origin est utilisé pour nom_lien
- Mettre la liaison en place  ``` $ git pull url_repository_github ```
- Préparer un/des fichiers(s) pour envoi sur Github ``` $ git add nom_fichier ``` ou * pour tous les fichiers
- Commiter les fichiers ``` $ git commit -m 'description commit' ```
- Envoyer commit sur Github avec le lien créé sur la branche choisie ``` $ git push nom_lien nom_branche ``` Généralement origin master
