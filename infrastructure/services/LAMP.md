# Installation / Configuration : [LAMP]

## 📌 Présentation
* **Description** : LAMP correspond à l'installation d'un stack serveur web sur Linux avec Apache, MySQL et PHP
* **Cible** : [serv02]
* **Prérequis** : OS installé, IP fixe configurée, accès internet

---

## 🛠️ Procédure d'installation

### 1. Préparation du système
> *Note : Toujours vérifier les mises à jour avant l'installation.*
* Étape A : Installation de Linux
* Étape B : Installation et configuration de Apache2
* Étape C : Installation et configuration de MySQL

### 2. Installation du rôle / logiciel
* **Commande** :

Apache2
```
sudo apt update && sudo apt install apache2
```

MySQL
```
sudo apt install mysql-server

#configuration mot de passe mysql
sudo

#configuration de sécurité initiale
sudo mysql_secure_install
```

PHPmyadmin
```
#installation des dépendances pour phpmyadmin
sudo apt install php libapache2-mod-php php-mysql

# installation et configuration de phpmyadmin
sudo apt install phpmyadmin
```

### 3.Validation (Screenshots)

![500](/assets/screenshots/lamp/lamp1.png)
![501](/assets/screenshots/lamp/lamp2.png)
![502](/assets/screenshots/lamp/lamp3.png)
![503](/assets/screenshots/lamp/lamp4.png)
![504](/assets/screenshots/lamp/lamp5.png)
![505](/assets/screenshots/lamp/lamp6.png)
![506](/assets/screenshots/lamp/lamp7.png)
![507](/assets/screenshots/lamp/lamp8.png)
![508](/assets/screenshots/lamp/lamp9.png)
![509](/assets/screenshots/lamp/lamp10.png)
