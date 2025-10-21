<p align="center">
  <img src="placeholder_link_to_logo.png" alt="VexoDNS Panel Logo" width="150"/> </p>
<h1 align="center">🛡️ Adguard DNS User Management Panel</h1>
<p align="center">
  A powerful, multi-user web panel for managing AdGuard Home with enhanced features like time/volume limits, automatic HTTPS, and SNI integration.
</p>
<p align="center">
  <img alt="Platform" src="https://img.shields.io/badge/platform-Linux%20(Debian%2FUbuntu)-orange.svg">
  <img alt="Backend" src="https://img.shields.io/badge/backend-Python%20Flask-blue.svg">
  <img alt="Frontend" src="https://img.shields.io/badge/frontend-HTML/CSS/JS-yellow.svg">
  <img alt="Database" src="https://img.shields.io/badge/database-SQLite-lightgrey.svg">
</p>

> [!NOTE]
> This panel provides a user-friendly interface for administrators to create and manage AdGuard Home clients, offering granular control over DNS usage through expiry dates and data volume quotas. It automatically generates secure DNS (DoT/DoH) links for users and integrates seamlessly with HAProxy for robust HTTPS support and SNI proxying capabilities.

---

## ✨ Key Features

* **👤 Client Management:** Create, edit, delete, enable/disable users.
* **⏱️ Time & Volume Limits:** Set expiry dates and data volume caps (GB) for each client. Unlimited options available.
* **🔗 Secure DNS Links:** Automatically generates unique DoT (DNS over TLS) and DoH (DNS over HTTPS) links for each client.
* **🔒 HTTPS Support:** Built-in integration with HAProxy for secure HTTPS access to the panel and DoH links using your own domain and SSL certificates.
* **📡 SNI Integration:** Automatically add/remove active client IPs to an external SNI proxy server (via SSH) to help bypass certain network restrictions.
* **🔄 Automatic IP Updates:** The user subscription page automatically detects the user's current IP address and updates it in AdGuard Home and the SNI server (if enabled).
* **🌐 Multi-Language Support:** Interface available in English, Farsi (Persian), Russian, and Chinese. User-preferred language is saved.
* **🎨 Theme Support:** Light and Dark mode options available, preference saved per user.
* **📊 Real-time Stats:** Dashboard displays live CPU/RAM usage via WebSockets.
* **⚙️ Comprehensive Settings:** Configure admin credentials, panel access (port/secret path), AdGuard Home connection, SSL certificates, and SNI server details.
* **📚 Integrated Guides:** Subscription page includes setup guides for iOS, Android, Windows, macOS, Linux, Game Consoles, Routers, and more.
* **💾 Backup & Restore:** Easily backup and restore the panel's database and configuration via the web interface.
* **🧹 Automatic Cleanup:** Background task to automatically manage expired or over-limit users.
* **⚡ Efficient Backend:** Uses Python Flask with Eventlet for efficient handling of concurrent connections and WebSockets.
* **🚀 Bulk Actions:** Extend expiry dates for multiple active users simultaneously.

## 📄 Subscription Page

Each user receives a unique subscription link (`/sub/<unique_token>`) which provides:

1.  **Automatic IP Registration:** Simply opening the page automatically detects the user's current IP address. If the user is active and the IP is new, it's instantly registered in AdGuard Home's allowed clients list and queued for the SNI server (if enabled).
2.  **Usage Information:** Displays remaining time, remaining data volume, total used data, and current status (Active, Expired, Disabled, Limited).
3.  **Connection Links:** Provides easy-to-copy DoT and DoH links, plus server IP addresses for DoU (DNS over UDP/QUIC) if configured.
4.  **Platform Guides:** Step-by-step instructions for configuring secure DNS on various operating systems and devices.

<p align="center">
  <img src="placeholder_link_to_sub_screenshot.png" alt="Subscription Page Screenshot" width="700"/>
  <br><em>(Replace placeholder_link_to_sub_screenshot.png with an actual screenshot URL)</em>
</p>

## 📱 Client Applications

While users can manually configure DNS settings using the guides on their subscription page, we recommend using the dedicated **VexoDNS** client applications for a simpler experience:

* **VexoDNS for Windows:** [![GitHub repo stars](https://img.shields.io/github/stars/Argo160/VexoDNSw?style=social)](https://github.com/Argo160/VexoDNSw) [https://github.com/Argo160/VexoDNSw](https://github.com/Argo160/VexoDNSw)
* **VexoDNS for Android:** [![GitHub repo stars](https://img.shields.io/github/stars/Argo160/VexoDNS?style=social)](https://github.com/Argo160/VexoDNS) [https://github.com/Argo160/VexoDNS](https://github.com/Argo160/VexoDNS)

These apps streamline the connection process for users.

## 📸 Screenshots

**Main Dashboard:**
<p align="center">
  <img src="placeholder_link_to_main_screenshot.png" alt="Main Dashboard Screenshot" width="700"/>
  <br><em>(Replace placeholder_link_to_main_screenshot.png with an actual screenshot URL)</em>
</p>

## 🛠️ Installation

Installation is handled via a bash script (`client-panell21.sh` provided separately) designed for Debian/Ubuntu systems. It sets up the Python environment, necessary services (Flask app, Helper service), HAProxy configuration, and permissions.

> [!WARNING]
> Root access (`sudo`) is required to run the installation script.

## 📜 Source Code & Future Development

Currently, the source code for AdGuard Panel Pro is not publicly available.

We plan to release the source code publicly once sufficient community support and funding are achieved through donations. Your contributions will directly support ongoing development, bug fixes, new features, and the eventual open-sourcing of the project.

## ❤️ Donate

If you find this panel useful and wish to support its development and public release, please consider donating:

* **USDT (BEP20 Network - BSC):**
    `0x3729348A169359a8Aa70a0627f3737aF4c6D1929`

<p align="center">
  <img src="https://img.shields.io/badge/USDT_(TRC20)-Donate-blue?logo=tether&color=26A17B" alt="Donate USDT TRC20"/>
</p>

Thank you for your support!
