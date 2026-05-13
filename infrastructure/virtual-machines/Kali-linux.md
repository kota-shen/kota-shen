# 🖥️ Fiche Technique : [kali-kota]

## 📝 Présentation
*   **Rôle :** Machine virtuelle de pentest
*   **Système d'exploitation :** Kali Linux
*   **Statut :** 🟢 Opérationnel

---

## ⚙️ Configuration VMWare (Hardware)
| Composant    | Paramètre           | Note                     |
| :----------- | :------------------ | :----------------------- |
| **ID VM**    | `9900`              | Suivi de l'inventaire    |
| **CPU**      | 4 vCPU (Type: Host) |                          |
| **RAM**      | 8 Go                | (Fixe ou Ballooning)     |
| **Disque**   | 300 Go              | Thin provisionning       |
| **Réseau**   | Bridge              | Pont vers Réseau proxmox |
| **BIOS/EFI** | Bios                |                          |

---

## 🌐 Configuration Réseau
*   **Adresse MAC :** `XX:XX:XX:XX:XX:XX`
*   **Mode IP :** (DHCP Statique / Statique manuelle)
*   **Adresse IP :** `10.0.0.X`
*   **Passerelle :** `10.0.0.1`
*   **DNS :** `10.0.0.1` (Proxmox/dnsmasq)

---

## 🛠️ Installation & Post-Configuration
- [x] Installation de l'OS via ISO.
- [x] Installation du Vmware Guest tools** (`apt install open-vm-tools).
- [x] Mises à jour système terminées.
- [x] Renommage du Hostname
- [ ] Snapshot "Clean Install" créé dans Proxmox.

---

## 📓 Notes de laboratoire
> *Note ici les problèmes rencontrés ou les réglages spécifiques (ex: désactivation du pare-feu Windows pour les tests ICMP initial).*