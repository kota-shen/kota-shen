# 🖥️ Fiche Technique : [wcl02]

## 📝 Présentation
*   **Rôle :** Poste de travail utilisateur
*   **Système d'exploitation :** Windows 11 Pro
*   **Statut :** 🟢 Opérationnel

---

## ⚙️ Configuration Proxmox (Hardware)
| Composant    | Paramètre           | Note                           |
| :----------- | :------------------ | :----------------------------- |
| **ID VM**    | `2002`              | Suivi de l'inventaire          |
| **CPU**      | 4 vCPU (Type: Host) | Utiliser 'Host' pour perf max  |
| **RAM**      | 4 Go                | Ballooning                     |
| **Disque**   | 128 Go (SATA)       |                                |
| **Réseau**   | `vmbr0` (VirtIO)    | Pont vers Flat Network         |
| **BIOS/EFI** | OVMF (UEFI)         | Requis pour Win11 / SecureBoot |

---

## 🌐 Configuration Réseau
*   **Adresse MAC :** `BC:24:11:71:02:F1`
*   **Mode IP :** DHCP
*   **Adresse IP :** `10.0.0.15`
*   **Passerelle :** `10.0.0.1`
*   **DNS :** `10.0.0.1` (Proxmox/dnsmasq)

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


![600](/assets/screenshots/windows11/win11-1.png)
![601](/assets/screenshots/windows11/win11-2.png)
![602](/assets/screenshots/windows11/win11-3.png)
![603](/assets/screenshots/windows11/win11-4.png)
![604](/assets/screenshots/windows11/win11-5.png)
![605](/assets/screenshots/windows11/win11-6.png)

