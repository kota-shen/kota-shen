# 🖥️ Fiche Technique : [fw]

## 📝 Présentation
*   **Rôle :** Firewall
*   **Système d'exploitation :** pfSense 2.7
*   **Statut :** 🟢 Opérationnel

---

## ⚙️ Configuration Proxmox (Hardware)
| Composant    | Paramètre                         | Note                          |
| :----------- | :-------------------------------- | :---------------------------- |
| **ID VM**    | `9904`                            | Suivi de l'inventaire         |
| **CPU**      | 1 vCPU (Type: Host)               | Utiliser 'Host' pour perf max |
| **RAM**      | 2 Go                              | Ballooning                    |
| **Disque**   | 32 Go (VirtIO Block)              | Cache: Write Back (Default)   |
| **Réseau**   | `vmbr0` (VirtIO) `vmbr1` (VirtIO) | Interface WAN & Trunk         |
| **BIOS/EFI** | SeaBIOS                           |                               |

---

## 🌐 Configuration Réseau
*   **Adresse MAC (WAN) :** `BC:24:11:F5:93:1D`
*   **Adresse MAC (LAN) :** `BC:24:11:9F:9B:DC`
*   **Mode IP :** DHCP sur WAN / Statique sur LAN
*   **Adresse IP :** `10.0.1.254`

---

## 🛠️ Installation & Post-Configuration
- [x] Installation de l'OS via ISO.
- [x] Configuration de Base flat network
- [ ] Snapshot "Clean Install" créé dans Proxmox.

---

## 📓 Notes de laboratoire
> *Note ici les problèmes rencontrés ou les réglages spécifiques (ex: désactivation du pare-feu Windows pour les tests ICMP initial).*



![800](/assets/screenshots/pfsense/pfsense1.png)
![801](/assets/screenshots/pfsense/pfsense2.png)
![802](/assets/screenshots/pfsense/pfsense3.png)
![803](/assets/screenshots/pfsense/pfsense4.png)
![804](/assets/screenshots/pfsense/pfsense5.png)
![805](/assets/screenshots/pfsense/pfsense6.png)
![806](/assets/screenshots/pfsense/pfsense7.png)
![807](/assets/screenshots/pfsense/pfsense8.png)
![808](/assets/screenshots/pfsense/pfsense9.png)