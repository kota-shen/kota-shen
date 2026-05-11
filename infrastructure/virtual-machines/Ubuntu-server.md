# 🖥️ Fiche Technique : [serv02]

## 📝 Présentation
*   **Rôle :** Serveur Web
*   **Système d'exploitation :** Ubuntu server 24.04
*   **Statut :** 🟢 Opérationnel

---

## ⚙️ Configuration Proxmox (Hardware)
| Composant    | Paramètre           | Note                          |
| :----------- | :------------------ | :---------------------------- |
| **ID VM**    | `1000`              | Suivi de l'inventaire         |
| **CPU**      | 4 vCPU (Type: Host) | Utiliser 'Host' pour perf max |
| **RAM**      | 2 Go                | Ballooning                    |
| **Disque**   | 64 Go (SATA)        |                               |
| **Réseau**   | `vmbr0` (VirtIO)    | Pont vers Flat Network        |
| **BIOS/EFI** | Seabios             |                               |

---

## 🌐 Configuration Réseau
*   **Adresse MAC :** `BC:24:11:AF:6E:E0`
*   **Mode IP :** Statique
*   **Adresse IP :** `10.0.0.46`
*   **Passerelle :** `10.0.0.1`
*   **DNS :** `10.0.0.1` (Proxmox/dnsmasq)

---

## 🛠️ Installation & Post-Configuration
- [x] Installation de l'OS via ISO.
- [x] Installation du **QEMU Guest Agent** (`apt install qemu-guest-agent`).
- [x] Mises à jour système terminées.
- [x] Renommage du Hostname (ex: `CLI-WIN10-01`).
- [x] Snapshot "Clean Install" créé dans Proxmox.

---

## 📓 Notes de laboratoire
> *Note ici les problèmes rencontrés ou les réglages spécifiques (ex: désactivation du pare-feu Windows pour les tests ICMP initial).*

![400](/assets/screenshots/ubuntuserver/ubuntuserv1.png)
![401](/assets/screenshots/ubuntuserver/ubuntuserv2.png)
![402](/assets/screenshots/ubuntuserver/ubuntuserv3.png)
![403](/assets/screenshots/ubuntuserver/ubuntuserv4.png)
![404](/assets/screenshots/ubuntuserver/ubuntuserv5.png)
![405](/assets/screenshots/ubuntuserver/ubuntuserv6.png)
![406](/assets/screenshots/ubuntuserver/ubuntuserv7.png)
![407](/assets/screenshots/ubuntuserver/ubuntuserv8.png)
![408](/assets/screenshots/ubuntuserver/ubuntuserv9.png)
![409](/assets/screenshots/ubuntuserver/ubuntuserv10.png)
![410](/assets/screenshots/ubuntuserver/ubuntuserv11.png)
