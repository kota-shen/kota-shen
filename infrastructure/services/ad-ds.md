
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

# Replication-active-directory

Dans ce labo j'ai mis en place un firewall pfsense afin d'y placer les machines composant l'infrastructure. Afin d'éviter une rupture de service, ou du moins minimiser l'impact, j'ai mis en oeuvre un second serveur windows pour que les machines ne soient pas coupées du domaine lors d'une migration.

- wsrv01 (Maître FSMO) : il se situe en amont du firewall (donc sur le réseau flat de départ)
- wsrv02 (Réplica) : Situé derrière le firewall
- Flux : Afin de permettre à l'infrastructure de fonctionner sans rupture, le firewall n'est pas encore durci afin de laisser passer les flux (RPC, DNS, Kerberos)

Une fois le nouveau serveur joint au domaine et le role active directory installé. Je vérifie que la réplication s'est effectuée sans encombre avec :

```
repadmin /showrepl
```

![900](/assets/screenshots/ad/ad08.png)
Validation de la réplication sans erreur

![901](/assets/screenshots/ad/ad09.png)
Visualisation des contrôleurs de domaine

Procédure de Validation (Test de "Failover")

Un test d'arrêt de l'AD-01 a été effectué. Le client Windows 10 a basculé automatiquement sur l'AD-02 pour la résolution DNS et l'authentification Kerberos, validant ainsi la continuité de service