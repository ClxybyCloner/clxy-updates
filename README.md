<p align="center">
  <img src="assets/banner.png" alt="CLXY — Fast. Private. Yours." width="100%">
</p>

<p align="center">
  <a href="https://github.com/ClxybyCloner/CLXY-Android/releases/latest"><img src="https://img.shields.io/github/v/release/ClxybyCloner/CLXY-Android?label=latest&color=7c5cff" alt="Latest release"></a>
  <a href="https://github.com/ClxybyCloner/CLXY-Android/releases"><img src="https://img.shields.io/badge/Android-7.0%2B-3DDC84?logo=android&logoColor=white" alt="Android 7.0+"></a>
  <img src="https://img.shields.io/badge/arch-arm64--v8a-4f8cff" alt="arm64-v8a">
  <a href="https://github.com/ClxybyCloner/CLXY-Android/releases"><img src="https://img.shields.io/github/downloads/ClxybyCloner/CLXY-Android/total?label=downloads" alt="Total downloads"></a>
</p>

<h1 align="center">CLXY — Official Android Releases</h1>
<p align="center"><b>Fast. Private. Yours.</b></p>

This is the **official download & update channel** for the CLXY Android app.
Every release is published here — and the in-app updater checks this exact
repository, so if you're running CLXY, you're always one tap away from the
newest build.

---

## ⬇️ Download

**Latest: 1.0.16**, released November 1, 2026

- 📦 [Download the APK (direct link)](https://github.com/ClxybyCloner/CLXY-Android/releases/download/v1.0.16/CLXY-1.0.16-Android-arm64-v8a.apk)
- 🗂️ [Browse all releases](https://github.com/ClxybyCloner/CLXY-Android/releases)

> ⚠️ Only download CLXY from this repository. Links from anywhere else are not official.

---

## Why CLXY

- 🌐 **Connection globe** — a live globe on the home screen showing your home country and your server country, linked by a glowing arc (based on IP info, not packet tracing).
- 📡 **Hotspot sharing** — share your connection with nearby devices over HTTP (`11811`) and SOCKS5 (`11812`) proxies, bound to your selected hotspot IP only.
- ⚡ **Live speeds** — real-time upload/download rates right in the Android notification.
- 📊 **Traffic & stats** — redesigned traffic cards, server picker, and account data usage with a one-tap jump to the stats page.
- 🌙 **Dark by design** — a locked-in dark theme across the whole app.
- 🔄 **In-app updater** — CLXY notifies you when a new build lands here. Downloading and installing always needs *your* confirmation — never silent.

---

## CLXY core architecture

CLXY pairs a Flutter interface with an embedded Go networking core. The core runs as a library inside the app. The UI uses a local bridge and loopback API to manage settings and read connection status, while the core handles network traffic.

In VPN mode, Android's `VpnService` creates a virtual TUN interface. A user-space TCP/IP stack processes packets and forwards TCP connections to the core's SOCKS5 proxy. The built-in DNS resolver maps domain names to temporary IP addresses so routing rules can still match domains. These rules choose whether to use the proxy, connect directly, or block a connection. App selection controls which apps use the VPN.

The core supports HTTP/2 CONNECT over TLS and HTTP/3 CONNECT over QUIC for connections to the gateway. Proxy-only mode uses the same core without creating a device-wide VPN. The Android VPN path handles TCP and DNS; other UDP traffic is not tunneled.

---

## Install in 60 seconds

1. **Download** the APK from the link above.
2. **Open it** — Android will ask you to allow *"Install unknown apps"* for your browser. Allow it once.
3. **Tap Install.** Done.

A subscription is required to use CLXY.

---

## ✅ Verify your download

On a computer, calculate the APK's SHA-256:

```bash
sha256sum CLXY-1.0.16-Android-arm64-v8a.apk
```

Compare the output with this expected hash:

```text
bf1d45ae48a4eb9ae6d37778d528941d65fa0472d3a421afdf9a108b0b1fe559  CLXY-1.0.16-Android-arm64-v8a.apk
```

If they match, the file is exactly what we published.

---

## 🔄 How updates work

CLXY periodically checks this repo's **Releases** for a newer version. When one
is found, you get a notification inside the app — tap it to download, then
confirm the install yourself. The app never installs anything behind your back.

---

## 📋 Current build specs

| | |
|---|---|
| Package | `com.clxy.android` |
| Version / version code | `1.0.16` / `8138` |
| Architecture | `arm64-v8a` |
| Minimum Android | 7.0 (API 24) |
| Size | ~20.3 MB |

---

## ❓ FAQ

**Is the source code here?**
No. This is a *distribution* repository — signed builds and update metadata only. The source code is not published.

**I need an older version.**
Older builds stay available on the [Releases page](https://github.com/ClxybyCloner/CLXY-Android/releases).

**The hotspot proxy asks for nothing — is that safe?**
The hotspot HTTP/SOCKS5 proxies have no password by design, so **only turn them on on a hotspot you trust**, and switch them off when you're done. Anyone connected to your hotspot could use them.

---

## 💬 Support

- 🌐 [clonerr.ir](https://clonerr.ir)
- ✈️ Telegram: [@cloner42](https://t.me/cloner42)

---

## 📜 Terms

© CLXY. All rights reserved. Please don't re-upload the app builds elsewhere —
link people here instead, so everyone always gets the genuine, verified build.

