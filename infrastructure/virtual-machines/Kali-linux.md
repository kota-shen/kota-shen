# 🖥️ Fiche Technique : [kali]

## 📝 Présentation
*   **Rôle :** (ex: Poste de travail utilisateur / Contrôleur de domaine)
*   **Système d'exploitation :** (ex: Windows 10 Pro 22H2)
*   **Statut :** 🟢 Opérationnel / 🟠 En cours / 🔴 Hors ligne

---

## ⚙️ Configuration Proxmox (Hardware)
| Composant       | Paramètre             | Note                          |
|:----------------|:----------------------|:------------------------------|
| **ID VM**       | `1XX`                 | Suivi de l'inventaire         |
| **CPU**         | X vCPU (Type: Host)   | Utiliser 'Host' pour perf max |
| **RAM**         | X Go                  | (Fixe ou Ballooning)          |
| **Disque**      | X Go (VirtIO Block)   | Cache: Write Back (Default)   |
| **Réseau**      | `vmbr0` (VirtIO)      | Pont vers Flat Network        |
| **BIOS/EFI**    | OVMF (UEFI)           | Requis pour Win11 / SecureBoot|

---

## 🌐 Configuration Réseau
*   **Adresse MAC :** `XX:XX:XX:XX:XX:XX`
*   **Mode IP :** (DHCP Statique / Statique manuelle)
*   **Adresse IP :** `10.0.0.X`
*   **Passerelle :** `10.0.0.1`
*   **DNS :** `10.0.0.1` (Proxmox/dnsmasq)

---

## 🛠️ Installation & Post-Configuration
- [ ] Installation de l'OS via ISO.
- [ ] Installation des **VirtIO Drivers** (pour Windows).
- [ ] Installation du **QEMU Guest Agent** (`apt install qemu-guest-agent`).
- [ ] Mises à jour système terminées.
- [ ] Renommage du Hostname (ex: `CLI-WIN10-01`).
- [ ] Snapshot "Clean Install" créé dans Proxmox.

---

## 📓 Notes de laboratoire
> *Note ici les problèmes rencontrés ou les réglages spécifiques (ex: désactivation du pare-feu Windows pour les tests ICMP initial).*