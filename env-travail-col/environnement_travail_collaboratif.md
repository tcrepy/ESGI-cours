Environnement de travail collaboratif
==
---

ssh
--
---
## Génération de la clé ssh

    ssh-keygen

## copie de la clé sur le serveur

    ssh-copy-id -i ~/.ssh/id_rsa.pub user@server

## ajouter un raccourci de connexion ssh


    nano ~/.ssh/config
    
    Host {name}
        HostName {ip}
        User {user}
        Port {port}
        IdentitiesOnly yes
        IdentityFile ~/.ssh/{private_key}
        
    ssh {name}


## Signer ses commits avec GPG

clé GPG : [lier avec github](https://medium.com/@timmywil/sign-your-commits-on-github-with-gpg-566f07762a43)



PR et issues
---
---
## Issues templates

Sur github, on peut selectionner un template d'issues

``Project > Settings > Set Up templates``

Ce sont des templates ecris en markdown.

On peut passer par l'interface web, ou sinon créer un dossier ``docs`` ou ``.github`` (le deuxième n'apparait pas si on fait un ls)

soit on a un seul template ``issue_template.md``

ou sinon on met les différents templates dans un dossier ``ÌSSUE_TEMPLATE/``
