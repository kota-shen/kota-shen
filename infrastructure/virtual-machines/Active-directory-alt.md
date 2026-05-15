# 🖥️ Fiche Technique : [wsrv02]

## 📝 Présentation
*   **Rôle :** Contrôleur de domaine secondaire
*   **Système d'exploitation :** Windows Server 2019
*   **Statut :** 🟢 Opérationnel

---

## ⚙️ Configuration Proxmox (Hardware)
| Composant    | Paramètre           | Note                          |
| :----------- | :------------------ | :---------------------------- |
| **ID VM**    | `3001`              | Suivi de l'inventaire         |
| **CPU**      | 1 vCPU (Type: Host) | Utiliser 'Host' pour perf max |
| **RAM**      | 2 Go                | Ballooning                    |
| **Disque**   | 128 Go (SATA)       |                               |
| **Réseau**   | `vmbr1` (VirtIO)    |                               |
| **BIOS/EFI** | SeaBIOS             |                               |

---

## 🌐 Configuration Réseau
*   **Adresse MAC :** `BC:24:11:6F:09:AE`
*   **Mode IP :** Statique manuelle
*   **Adresse IP :** `10.0.1.10`
*   **Passerelle :** `10.0.1.254`
*   **DNS :** `10.0.1.254`

---

## 🛠️ Installation & Post-Configuration
- [x] Installation de l'OS via ISO.
- [x] Installation des **VirtIO Drivers** (pour Windows).
- [x] Mises à jour système terminées.
- [x] Renommage du Hostname (ex: `CLI-WIN10-01`).
- [x] Snapshot "Clean Install" créé dans Proxmox.

---

## 📓 Notes de laboratoire
> *Note ici les problèmes rencontrés ou les réglages spécifiques (ex: désactivation du pare-feu Windows pour les tests ICMP initial).*

