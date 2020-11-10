# Bac à Sable pour NSI

1. Faites un *fork* de ce dépôt,

2. cloner votre fork sur votre ordinateur de travail (installer git préalablement!)
       
       git clone <url_mon_fork>

3. Dans votre copie locale (sur votre ordinateur de travail):
   
   a. Configurer git (si ce n'est pas déjà fait):
       
       git config --global user.name <votre_login>
       git config --global user.email <votre_email>
   
   b. Configurer le suivi du dépôt principal (celui-ci):
   
       git remote add principal https://github.com/efloti/bac_a_sable
       git fetch
       git branch --set-upstream-to=principal/master master
       git pull
   
   c. Créer une branche de contribution et placez-vous dessus:
   
       git branch contrib
       git checkout contrib
   
   d. Ajouter un fichier avec un peu de code python ou du texte puis valider le:
   
       git add <mon_fichier>
       git commit -m "<mon_message_de_validation>"
   
   e. Pousser votre contribution sur votre «fork» (nommé automatiquement *origin* lors du clonage):
   
       git push origin contrib
   
   d. Aller sur votre fork sur github et lancer une «**pull-request**» (requête de tirage).

4. Un peu plus tard ... mettez à jour votre dépôt:

       git checkout master
       git pull

5. Puis votre branch contrib:

       git checkout contrib
       git merge master

6. Vous êtes prêt à recommencer le cycle depuis l'étape **3 d** après avoir «synchroniser» votre dépôt local:

        git checkout master
        git pull
        git checkout contrib
        git merge master
        ... prêt à travailler à nouveau ...
