<p align="center">
  <a href="README_fa.md"><img src="assets/language-fa.svg" alt="نسخه فارسی" width="180"></a>
</p>

<p align="center">
  <img src="assets/banner.png" alt="CLXY: Fast. Private. Yours." width="100%">
</p>

<p align="center">
  <a href="https://github.com/ClxybyCloner/CLXY-Android/releases/latest"><img src="https://img.shields.io/github/v/release/ClxybyCloner/CLXY-Android?label=latest&color=7c5cff" alt="Latest release"></a>
  <a href="https://github.com/ClxybyCloner/CLXY-Android/releases"><img src="https://img.shields.io/badge/Android-7.0%2B-3DDC84?logo=android&logoColor=white" alt="Android 7.0+"></a>
  <img src="https://img.shields.io/badge/arch-arm64--v8a-4f8cff" alt="arm64-v8a">
  <a href="https://github.com/ClxybyCloner/CLXY-Android/releases"><img src="https://img.shields.io/github/downloads/ClxybyCloner/CLXY-Android/total?label=downloads" alt="Total downloads"></a>
</p>

<h1 align="center">CLXY: Official Android Releases</h1>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&duration=2800&pause=1200&color=7C5CFF&center=true&vCenter=true&width=700&lines=Fast.+Private.+Yours.;Official+CLXY+Android+releases;One+tap+away+from+the+newest+build" alt="Fast. Private. Yours.">
</p>

This repository is the **official download and update channel** for the CLXY
Android app. Every release is published here. The in-app updater checks this
repository for new builds.

<p align="center">
  <img src="assets/wave.svg" alt="" width="100%">
</p>

## ⬇️ Download

**Latest: 1.0.16**, released November 1, 2026

- 📦 [Download the APK (direct link)](https://github.com/ClxybyCloner/CLXY-Android/releases/download/v1.0.16/CLXY-1.0.16-Android-arm64-v8a.apk)
- 🗂️ [Browse all releases](https://github.com/ClxybyCloner/CLXY-Android/releases)

> ⚠️ Only download CLXY from this repository. Links from anywhere else are not official.

---

## Why CLXY

- 🌐 The home screen shows a live globe with your home and server countries linked by a glowing arc. It uses IP information, not packet tracing.
- 📡 Share your connection with nearby devices over HTTP (`11811`) and SOCKS5 (`11812`). Both proxies bind only to the hotspot IP you selected.
- ⚡ Android notifications show live upload and download rates.
- 📊 Redesigned traffic cards, the server picker, and account data usage make it easy to check your stats. Tap a traffic card to open the stats page.
- 🌙 The app uses a dark theme throughout.
- 🔄 CLXY notifies you when a new build is available here. Downloading and installing require your confirmation.

---

## CLXY core architecture

CLXY pairs a Flutter interface with an embedded Go networking core. The core runs as a library inside the app. The UI uses a local bridge and loopback API to manage settings and read connection status, while the core handles network traffic.

In VPN mode, Android's `VpnService` creates a virtual TUN interface. A user-space TCP/IP stack processes packets and forwards TCP connections to the core's SOCKS5 proxy. The built-in DNS resolver maps domain names to temporary IP addresses so routing rules can still match domains. These rules choose whether to use the proxy, connect directly, or block a connection. App selection controls which apps use the VPN.

The core supports HTTP/2 CONNECT over TLS and HTTP/3 CONNECT over QUIC for connections to the gateway. Proxy-only mode uses the same core without creating a device-wide VPN. The Android VPN path handles TCP and DNS; other UDP traffic is not tunneled.

---

## Install in 60 seconds

1. **Download** the APK from the link above.
2. **Open the APK.** Android will ask you to allow your browser to *"Install unknown apps"*. Allow it once.
3. **Tap Install** to finish.

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

CLXY periodically checks this repository's **Releases** for a newer version.
When one is available, the app notifies you. Tap the notification to download
the update, then confirm the installation. CLXY does not install updates
automatically.

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
No. This repository is for distribution only. It contains signed builds and
update metadata, not source code.

**I need an older version.**
Older builds stay available on the [Releases page](https://github.com/ClxybyCloner/CLXY-Android/releases).

**The hotspot proxy asks for nothing. Is that safe?**
The hotspot HTTP/SOCKS5 proxies have no password by design. **Turn them on only
when you trust the hotspot**, and switch them off when you're done. Anyone
connected to the hotspot can use them.

---

## 💬 Support

- 🌐 [clonerr.ir](https://www.clonerr.ir)
- ✈️ Telegram: [@cloner42](https://t.me/cloner42)

<p align="center">
  <img src="assets/wave.svg" alt="" width="100%">
</p>

## 📜 Terms

© CLXY. All rights reserved. Please don't re-upload the app builds. Share this
repository's link so people can download the genuine, verified build.
