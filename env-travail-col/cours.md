ssh
===

### Génération de la clé ssh

    ssh-keygen

### copie de la clé sur le serveur

    ssh-copy-id -i ~/.ssh/id_rsa.pub user@server

### ajouter un raccourci de connexion ssh


    nano ~/.ssh/config
    
    Host {name}
        HostName {ip}
        User {user}
        Port {port}
        IdentitiesOnly yes
        IdentityFile ~/.ssh/{private_key}
        
    ssh {name}
    

### Signer ses commits avec GPG

clé GPG : [lier avec github](https://medium.com/@timmywil/sign-your-commits-on-github-with-gpg-566f07762a43)
    
