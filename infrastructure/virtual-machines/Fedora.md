# 🖥️ Fiche Technique : [cl02]

## 📝 Présentation
*   **Rôle :** Poste de travail utilisateur
*   **Système d'exploitation :** Fedora 44
*   **Statut :** 🟢 Opérationnel / 🟠 En cours / 🔴 Hors ligne

---

## ⚙️ Configuration Proxmox (Hardware)
| Composant    | Paramètre           | Note                           |
| :----------- | :------------------ | :----------------------------- |
| **ID VM**    | `2003`              | Suivi de l'inventaire          |
| **CPU**      | 4 vCPU (Type: Host) | Utiliser 'Host' pour perf max  |
| **RAM**      | 4 Go                | Ballooning                     |
| **Disque**   | 64 Go (SATA)        |                                |
| **Réseau**   | `vmbr0` (VirtIO)    | Pont vers Flat Network         |
| **BIOS/EFI** | SeaBIOS             | Requis pour Win11 / SecureBoot |

---

## 🌐 Configuration Réseau
*   **Adresse MAC :** `BC:24:11:FF:69:E1`
*   **Mode IP :** DHCP
*   **Adresse IP :** `10.0.0.58`
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