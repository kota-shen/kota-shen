# 👋 Bonjour, je m'appelle Aurélien (kota-shen)
### 🛠️ Administrateur Systèmes & Réseaux | 🛡️ Auditeur Cybersécurité Freelance

<p align="left">
<a href="https://www.linkedin.com/in/aurelien-pardons/"><img src="https://img.shields.io/badge/-LinkedIn-0072b1?&style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:aurelien.pardons@hotmail.com"><img src="https://img.shields.io/badge/-Contact-D14836?&style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

---

## 🎓 Certifications & Diplômes
| Certification            | Badge                                                                                                     |
| :----------------------- | :-------------------------------------------------------------------------------------------------------- |
| **Google IT Support** | ![Google](https://img.shields.io/badge/Professional-4285F4?style=flat-square&logo=google&logoColor=white) |
| **IFAPME E6K Cyber** | ![E6K](https://img.shields.io/badge/Graduate-FFD700?style=flat-square&logo=education&logoColor=black)     |
| **Blue Team Jr Analyst** | ![BTJA](https://img.shields.io/badge/BTJA-0072b1?style=flat-square)                                       |

---

## 🏗️ Mobile Audit Kit, HomeLab & Virtual Lab (EVE-NG)
> Ma configuration simule une intervention d'audit réelle : une station mobile interagissant avec une infrastructure d'entreprise virtualisée (systèmes et réseau d'entreprise complexe).

![schéma.png](./assets/diagrams/schéma.png)

### 🛡️ Station d'Audit (Physique & VM)
* **Systèmes :** Kali Linux (Rolling) & CSI Linux (Investigation).
* **Outils :** Greenbone (OpenVAS), TL Osint, Nmap, Wireshark, Python.

### 🌐 Infrastructure Réseau & Sécurité (Hybride Proxmox / EVE-NG)
* **Architecture Réseau Émulée (EVE-NG) :** Équipements **Cisco** (Routeur + Switch) configurés initialement en réseau plat (VLAN unique) pour interconnecter et distribuer le réseau au lab.
* **Sécurité & Pare-feu (EVE-NG) :** Appliance **Fortigate** intégrée dans un second temps pour assurer la transition vers une architecture réseau segmentée (Routage inter-VLAN) et des politiques de sécurité d'entreprise strictes.
* **Systèmes (Proxmox) :** Active Directory (Win Server), Multi-OS (Win 10/11, Ubuntu, Fedora).
* **Observabilité :** Zabbix & GLPI.

---

## 🛠️ Stack Technique
| Catégorie | Badges |
| :--- | :--- |
| **Cybersécurité** | ![Greenbone](https://img.shields.io/badge/Greenbone-77AD1E?style=flat-square&logo=openvas&logoColor=white) ![CSI Linux](https://img.shields.io/badge/CSI%20Linux-000000?style=flat-square&logo=linux) ![OSINT](https://img.shields.io/badge/OSINT-TL%20Osint-blue?style=flat-square) ![Fortinet](https://img.shields.io/badge/Fortinet-FF0000?style=flat-square&logo=fortinet&logoColor=white) |
| **Systèmes** | ![Win](https://img.shields.io/badge/Windows-0078D6?style=flat-square&logo=windows) ![Linux](https://img.shields.io/badge/Linux-E95420?style=flat-square&logo=linux) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker) |
| **Réseau & Lab** | ![EVE-NG](https://img.shields.io/badge/EVE--NG-Orange?style=flat-square) ![Cisco](https://img.shields.io/badge/Cisco-00bce1?style=square&logo=cisco&logoColor=white) |
| **Monitoring** | ![Zabbix](https://img.shields.io/badge/Zabbix-FF6600?style=flat-square&logo=zabbix) ![GLPI](https://img.shields.io/badge/GLPI-green?style=flat-square) |

---

## 🚀 Roadmap de Déploiement
- [x] **Phase 0 :** [Proxmox Hypervisor setup (NAT routing & DHCP)](./infrastructure/proxmox/network-setup.md)
	- [x] Inventaire initial : [Fichier PDF](./documentation/inventory/Inventaire.pdf)
- [ ] **Phase 1 :** Initialisation du Lab Réseau (EVE-NG)
	- [ ] Déploiement d'EVE-NG directement sur Proxmox
	- [ ] Configuration de la topologie initiale : **1 Routeur Cisco + 1 Switch Cisco**
	- [ ] Instanciation d'un **réseau plat (un seul VLAN)** faisant office de passerelle permissive pour démarrer le lab
- [ ] **Phase 2 :** Déploiement Win 10 Pro & Windows Server AD DS (GPO, DNS).
	- [ ] Déploiement Windows 10 Pro
	- [ ] Déploiement Windows Serveur]
	- [ ] Installation et configuration de l'Active Directory
- [ ] **Phase 3 :** Déploiement Ubuntu Desktop & Ubuntu serveur
	- [ ] Déploiement Ubuntu Desktop
	- [ ] Déploiement Ubuntu Serveur
	- [ ] Installation et configuration de LAMP
- [ ] **Phase 4 :** Déploiement Windows 11 & Fedora (Prep LPI Essentials).
	- [ ] Déploiement de Windows 11
	- [ ] Déploiement de Fedora 44
- [ ] **Phase 5 :** Extension Active Directory
	- [ ] Déploiement second Active Directory
	- [ ] Réplication Active Directory]
- [ ] **Phase 6 :** Évolution de la Topologie & Hardening (Fortigate & Cisco avancé)
	- [ ] Intégration et configuration du Firewall Fortigate dans la topologie EVE-NG
	- [ ] Création des VLANs, migration vers un routage inter-VLAN et mise en place des politiques restrictives
- [ ] **Phase 7 :** Audit de l'infrastructure (Systèmes & Réseau)
- [ ] **Phase 8 :** Déploiement Docker
- [ ] **Phase 9 :** Mise sous contrôle avec GLPI & Zabbix (Monitoring des serveurs + Équipements Cisco/Fortigate via SNMP)
- [ ] **Phase 10 :** Sécurité avancée SIEM, IDS/IPS, Proxy

---

## 🎯 Objectif Business
Lancer mon activité de **Consultant en Cybersécurité**. Ce projet sert de "Proof of Concept" pour démontrer ma capacité à auditer, sécuriser et monitorer un parc informatique de PME de A à Z, en m'appuyant sur des topologies réseau constructeurs majeures (Cisco, Fortinet) émulées pour coller aux environnements de production réels.

---
<p align="center">
  <i>"Comprendre le système pour mieux le protéger."</i>
</p>