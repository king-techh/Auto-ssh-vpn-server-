# 🔥 TOXIC VPN Server Menu v3.0

Premium VPN/SSH server management menu for VPS — SSH, V2Ray, Dropbear, OpenVPN, SSL, Domain pointing, all in one script with a beautiful terminal UI.

## 🚀 Installation

```bash
# Clone from GitHub
git clone https://github.com/king-techh/Auto-ssh-vpn-server-.git

# Run the menu
cd toxic-vpn-menu
sudo bash toxic-menu
```

## ⚡ Quick Auto-Install Everything

```bash
sudo bash toxic-menu
# Select option 9 — Auto Install All
```

Installs: SSH + Dropbear + V2Ray + Nginx + Certbot + Fail2Ban + UFW

## 🎮 Main Menu

```
  ╔════════════════════════════════════════╗
  ║ 🔥 MAIN MENU                          ║
  ╠════════════════════════════════════════╣
  ║ 1) SSH Menu                            ║
  ║ 2) V2Ray Menu                          ║
  ║ 3) Dropbear Menu                       ║
  ║ 4) OpenVPN Menu                        ║
  ║ 5) SSL/TLS Menu                        ║
  ║ 6) Domain Setup                        ║
  ║ 7) User Management                     ║
  ║ 8) System Info                         ║
  ║ 9) Auto Install All                    ║
  ║ 0) Exit                                ║
  ╚════════════════════════════════════════╝
```

## 📋 Services

| Service | Features |
|---------|----------|
| **SSH** | Install, configure port, create accounts, speed limit |
| **V2Ray** | VMess, VLESS, WS+TLS, gRPC — generates share links |
| **Dropbear** | Lightweight SSH on port 443, separate accounts |
| **OpenVPN** | One-click install, user create/revoke |
| **SSL/TLS** | Let's Encrypt, self-signed, auto-renew |
| **Domain** | Set domain, Cloudflare guide, Nginx reverse proxy |
| **Users** | Create, delete, expiry, lock/unlock for all services |

## 🌐 Domain Setup Flow

1. **Point your domain** to your VPS IP (A record in Cloudflare/DNS)
2. **Set domain** in menu option 6
3. **Generate SSL** in menu option 5
4. **Configure Nginx** reverse proxy for V2Ray WS+TLS
5. **Create V2Ray WS+TLS account** — gets shareable link

## 🔗 V2Ray Links

The script generates ready-to-use V2Ray links:
- **VMess links** — `vmess://base64...`
- **VLESS links** — `vless://uuid@ip:port?...`

Import directly into V2RayNG (Android), V2rayN (Windows), Shadowrocket (iOS)

## 🛡️ Security

- Fail2Ban auto-bans after 3 failed attempts
- UFW firewall only allows needed ports
- SSH hardening (no root, max 3 attempts)
- SSL/TLS for all V2Ray connections

## 🖥️ Supported OS

- ✅ Ubuntu 18.04 / 20.04 / 22.04 / 24.04
- ✅ Debian 10 / 11 / 12
- ✅ CentOS 7/8/9, RHEL, Fedora

## 📁 File Structure

```
/etc/toxic-vpn/           # Config directory
├── accounts.db           # User accounts database
├── domain.conf           # Domain setting
├── settings.conf         # General settings
├── ssh_port.conf         # SSH port
├── ssh_speed.conf        # Speed limit
└── ssl/                  # SSL certificates
    ├── fullchain.pem
    └── privkey.pem
```

---
🔥 **TOXIC VPN Menu** — Premium VPN server tools by ToxicTech
