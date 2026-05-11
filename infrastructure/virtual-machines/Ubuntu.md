# 🖥️ Fiche Technique : [cl01]

## 📝 Présentation
*   **Rôle :** Poste de travail utilisateur
*   **Système d'exploitation :** Ubuntu 22.04.4
*   **Statut :** 🟢 Opérationnel

---

## ⚙️ Configuration Proxmox (Hardware)
| Composant    | Paramètre           | Note                          |
| :----------- | :------------------ | :---------------------------- |
| **ID VM**    | `2001`              | Suivi de l'inventaire         |
| **CPU**      | 4 vCPU (Type: Host) | Utiliser 'Host' pour perf max |
| **RAM**      | 4 Go                | Ballooning                    |
| **Disque**   | 64 Go (SATA)        |                               |
| **Réseau**   | `vmbr0` (VirtIO)    | Pont vers Flat Network        |
| **BIOS/EFI** | SEABIOS             |                               |

---

## 🌐 Configuration Réseau
*   **Adresse MAC :** `BC:24:11:8B:98:18`
*   **Mode IP :** DHCP
*   **Adresse IP :** `10.0.0.91`
*   **Passerelle :** `10.0.0.1`
*   **DNS :** `10.0.0.1` (Proxmox/dnsmasq)

---

## 🛠️ Installation & Post-Configuration
- [x] Installation de l'OS via ISO.
- [x] Installation du **QEMU Guest Agent** (`apt install qemu-guest-agent`).
- [x] Mises à jour système terminées.
- [x] Renommage du Hostname
- [x] Snapshot "Clean Install" créé dans Proxmox.

---

## 📓 Notes de laboratoire
> *Note ici les problèmes rencontrés ou les réglages spécifiques (ex: désactivation du pare-feu Windows pour les tests ICMP initial).*


![382](/assets/screenshots/ubuntu/ubuntu1.png)
![383](/assets/screenshots/ubuntu/ubuntu2.png)
![384](/assets/screenshots/ubuntu/ubuntu3.png)
![385](/assets/screenshots/ubuntu/ubuntu4.png)
![386](/assets/screenshots/ubuntu/ubuntu5.png)
![387](/assets/screenshots/ubuntu/ubuntu6.png)