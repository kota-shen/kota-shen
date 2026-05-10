
# Installation / Configuration : [Active Directory]

## 📌 Présentation
* **Description** : Domain controller
* **Cible** : [wsrv01]
* **Prérequis** : OS installé, IP fixe configurée, accès réseau

---

## 🛠️ Procédure d'installation

### 1. Préparation du système
> *Note : Toujours vérifier les mises à jour avant l'installation.*
* Étape A : Fixation de l'adresse IP
![1](/assets/screenshots/ad/ad01.png)


### 2. Installation du rôle / logiciel
* **Commande (si applicable)** :

```
Install-WindowsFeature -Name AD-Domain-Services -IncludeManagementTools
```

- **Configuration via GUI** :
![2](/assets/screenshots/ad/ad02.png)
![3](/assets/screenshots/ad/ad03.png)
![4](/assets/screenshots/ad/ad04.png)

![5](/assets/screenshots/ad/ad05.png)
![6](/assets/screenshots/ad/ad06.png)
![7](/assets/screenshots/ad/ad07.png)

---

## 🔄 État du Lab & Snapshot

- **Nom du Snapshot** : `Post-install-AD`
    
- **Date** : 09/05/2026