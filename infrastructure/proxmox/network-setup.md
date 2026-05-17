#### **# Proxmox Hypervisor: Network & Routing Configuration**

**Goal:** Provide internet access to the `vmbr0` internal bridge via the host's Wi-Fi interface (wlan0) and automate IP assignment for VMs using `dnsmasq`.

---

#### **## 🌐 Network Topology**

- **Host Interface:** `wlp...` (Wi-Fi connected to Internet)
    
- **Internal Bridge:** `vmbr0` (Virtual switch for VMs)
    
- **Subnet:** `10.0.0.0/24`
    
- **Gateway (Proxmox IP on bridge):** `10.0.0.1`
    

---

#### **## 🛠️ Implementation Steps**

##### **1. Interface Configuration (`/etc/network/interfaces`)**


```
auto vmbr0
iface vmbr0 inet static
    address 10.0.0.1/24
    bridge-ports none
    bridge-stp off
    bridge-fd 0
```

##### **2. IP Forwarding & NAT (IPtables)**

Bash

```
# Enable IP Forwarding
sysctl -w net.ipv4.ip_forward=1

# NAT Rule (Replace wlan0 with your interface)
iptables -t nat -A POSTROUTING -o wlan0 -j MASQUERADE
```


##### **3. DHCP & DNS with Dnsmasq**

Connectez-vous en SSH ou via la console Proxmox et lancez :

```
apt update
apt install dnsmasq -y
```

Nous allons créer un fichier de configuration propre. Je vous conseille de vider le fichier par défaut ou d'en créer un nouveau :

`nano /etc/dnsmasq.d/proxmox-nat.conf`

Collez-y la configuration suivante (en l'adaptant à votre plage d'IP définie précédemment) :


```
# Ne pas écouter sur le Wi-Fi (important pour la sécurité)
interface=vmbr0
bind-interfaces

# Plage DHCP : de .10 à .100 avec un bail de 12h
dhcp-range=10.0.0.10,10.0.0.100,255.255.255.0,12h

# Définir la passerelle par défaut pour les VMs
dhcp-option=option:router,10.0.0.1

# Définir le serveur DNS pour les VMs (l'hôte lui-même ou Google/Cloudflare)
dhcp-option=option:dns-server,10.0.0.1,8.8.8.8

# Log les requêtes pour le débug (optionnel)
log-facility=/var/log/dnsmasq.log
log-queries
log-dhcp
```

Redémarrez dnsmasq pour appliquer vos changements :

```
systemctl restart dnsmasq
systemctl enable dnsmasq
```

