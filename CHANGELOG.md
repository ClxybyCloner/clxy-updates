# CLXY Android — Changelog

All notable changes to the CLXY Android app, newest first.
Every version below is available as a GitHub Release with its signed APK.

| Version | Date | Release notes |
|---|---|---|
| **1.0.15** | 2026-10-29 | [v1.0.15](https://github.com/ClxybyCloner/CLXY-Android/releases/tag/v1.0.15) |
| 1.0.10 | 2026-10-29 | [v1.0.10](https://github.com/ClxybyCloner/CLXY-Android/releases/tag/v1.0.10) |
| 1.0.9 | 2026-10-27 | [v1.0.9](https://github.com/ClxybyCloner/CLXY-Android/releases/tag/v1.0.9) |
| 1.0.8 | 2026-10-27 | [v1.0.8](https://github.com/ClxybyCloner/CLXY-Android/releases/tag/v1.0.8) |
| 1.0.7 | 2026-10-27 | [v1.0.7](https://github.com/ClxybyCloner/CLXY-Android/releases/tag/v1.0.7) |
| 1.0.6 | 2026-10-27 | [v1.0.6](https://github.com/ClxybyCloner/CLXY-Android/releases/tag/v1.0.6) |
| 1.0.5 | 2026-10-27 | [v1.0.5](https://github.com/ClxybyCloner/CLXY-Android/releases/tag/v1.0.5) |
| 1.0.4 | 2026-10-26 | [v1.0.4](https://github.com/ClxybyCloner/CLXY-Android/releases/tag/v1.0.4) |

---

## 1.0.15 — 2026-10-29

Home-screen redesign, built around a new connection experience:

- Space-themed home screen with a brand-new connection globe and connect button.
- The globe shows your home country and server country separately, linked by glowing markers and a light arc. (Based on IP information — not real packet-path tracing.)
- Redesigned traffic, server-picker, and account data cards; the traffic card now jumps straight to the stats page.
- Refreshed mobile header and bottom bar, with account and settings shortcuts in the header and the official CLXY logo unified across the app.
- Smooth fade-and-slide animations between tabs and pages.

`arm64-v8a` · package `com.clxy.android` · version code `8137` · same package and signing certificate as 1.0.10 — installs over it, no uninstall needed.

## 1.0.10 — 2026-10-29

- Live upload and download rates now appear in the persistent Android notification.
- Existing installs migrate the notification-speed setting to on once; it stays user-adjustable.

## 1.0.9 — 2026-10-27

- Dark theme is now locked in — the app no longer follows the system light/dark mode; the old saved preference is cleared.
- The in-app updater is connected to the official Android release repository.
- Version code `2127` → `2128`. Package and signing certificate unchanged.
- All 145 Flutter tests, `flutter analyze`, and the full Go 1.27.2 test suite passed.

## 1.0.8 — 2026-10-27

- Separate SOCKS5 proxy for hotspot-connected devices (default port `11812`); the HTTP proxy stays on `11811`.
- Both proxies bind only to the selected private hotspot IP. Main CLXY proxy settings are untouched.
- SOCKS5 passes TCP CONNECT only (no UDP ASSOCIATE); on the Mozilla route only destination ports `80`, `443`, `8080`, `8443` are allowed.

## 1.0.7 — 2026-10-27

- Hotspot IP detection fix for `is not assigned to active interface "swlan0"` — falls back to a kernel-level (ioctl) check of the interface address when Go's address list misses the hotspot IP. Never falls back to a wildcard or another interface's IP.
- Installs over 1.0.6, no uninstall needed.

## 1.0.6 — 2026-10-27

- Hotspot IP picker no longer offers VPN interfaces like `tun0`; sharing is refused when only a VPN address is available.

## 1.0.5 — 2026-10-27

- New package `com.clxy.android` (version code `2124`) — first build under the CLXY identity.
- Hotspot HTTP proxy listens only on the selected private IP — never on a wildcard.
- 132 Flutter tests, code analysis, and Go 1.27.2 tests passed. Same signing certificate as the previous build.

> ⚠️ **Hotspot proxy security note (applies to 1.0.5+):** the hotspot HTTP/SOCKS5 proxies have no password. Any device connected to your hotspot can use them — only enable them on a hotspot you trust, and turn them off when you're done.

## 1.0.4 — 2026-10-26

- First public CLXY-branded Android release, `arm64-v8a`.
- SHA-256: `4a6cce6f0fd16966a1c26e9e8c32fa59577b2d2619721cd4e776494e48186132`
