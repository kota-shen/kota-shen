# 🖥️ Fiche Technique : [Windows 10]

## 📝 Présentation
*   **Rôle :** Poste de travail utilisateur
*   **Système d'exploitation :** Windows 10 Pro 22H2
*   **Statut :** 🟢 Opérationnel

---

## ⚙️ Configuration Proxmox (Hardware)
| Composant    | Paramètre           | Note                          |
| :----------- | :------------------ | :---------------------------- |
| **ID VM**    | `2000`              | Suivi de l'inventaire         |
| **CPU**      | 4 vCPU (Type: Host) | Utiliser 'Host' pour perf max |
| **RAM**      | 4 Go                | Ballooning                    |
| **Disque**   | 128 Go (SATA)       |                               |
| **Réseau**   | `vmbr0` (VirtIO)    | Pont vers Flat Network        |
| **BIOS/EFI** | OVMF (UEFI)         |                               |

---

## 🌐 Configuration Réseau
*   **Adresse MAC :** `bc:24:11:98:29:5e`
*   **Mode IP :** DHCP
*   **Adresse IP :** `10.0.0.37`
*   **Passerelle :** `10.0.0.1`
*   **DNS :** `10.0.0.1` (Proxmox/dnsmasq)

---

## 🛠️ Installation & Post-Configuration
- [x] Installation de l'OS via ISO.
- [x] Installation des **VirtIO Drivers** (pour Windows).
- [x] Mises à jour système terminées.
- [x] Renommage du Hostname (wcl01).
- [x] Snapshot "Clean Install" créé dans Proxmox.

---

## 📓 Notes de laboratoire
> *Note ici les problèmes rencontrés ou les réglages spécifiques (ex: désactivation du pare-feu Windows pour les tests ICMP initial).*

![[../../assets/screenshots/windows10/windows10-1.png]]

![[../../assets/screenshots/windows10/windows10-2.png]]

![[../../assets/screenshots/windows10/windows10-3.png]]

![[../../assets/screenshots/windows10/windows10-4.png]]

![[../../assets/screenshots/windows10/windows10-5.png]]

![[../../assets/screenshots/windows10/windows10-6.png]]

![[../../assets/screenshots/windows10/windows10-7.png]]

![[../../assets/screenshots/windows10/windows10-8.png]]

![[../../assets/screenshots/windows10/windows10-9.png]]

![[../../assets/screenshots/windows10/windows10-10.png]]

![[../../assets/screenshots/windows10/windows10-11.png]]

![[../../assets/screenshots/windows10/windows10-12.png]]

![[../../assets/screenshots/windows10/windows10-13.png]]

![[../../assets/screenshots/windows10/windows10-14.png]]

![[../../assets/screenshots/windows10/windows10-15.png]]

![[../../assets/screenshots/windows10/windows10-16.png]]

![[../../assets/screenshots/windows10/windows10-17.png]]

![[../../assets/screenshots/windows10/windows10-18.png]]

![[../../assets/screenshots/windows10/windows10-19.png]]
