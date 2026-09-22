# Duo Status Bar

[![Downloads](https://img.shields.io/github/downloads/kvmy666/duoStatusBar/total?label=downloads)](https://github.com/kvmy666/duoStatusBar/releases)
[![Latest release](https://img.shields.io/github/v/release/kvmy666/duoStatusBar)](https://github.com/kvmy666/duoStatusBar/releases)
[![CI](https://github.com/kvmy666/duoStatusBar/actions/workflows/ci.yml/badge.svg)](https://github.com/kvmy666/duoStatusBar/actions/workflows/ci.yml)
[![Android 15+](https://img.shields.io/badge/Android-15%2B-3ddc84)](https://developer.android.com)
[![LSPosed](https://img.shields.io/badge/LSPosed-module-8a2be2)](https://modules.lsposed.org/module/io.github.kvmy666.duostatusbar)

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/kvmy666/duoStatusBar@main/docs/media/icon.png" width="120" alt="Duo Status Bar icon">
</p>

**Your status bar, but beautiful.** Duo Status Bar turns the battery, Wi-Fi and signal icons into one
smooth, Apple-style element — a battery ring with the percentage tucked into its gap, Wi-Fi arcs, cellular
spheres and a charging bolt that flies into place. It is animated with [Rive](https://rive.app), and it is
built to be switched off the instant you want your old bar back.

No system files are touched. Nothing is patched. The module only *draws*.

<img src="https://cdn.jsdelivr.net/gh/kvmy666/duoStatusBar@main/docs/media/status-bar.png" width="360" alt="The Duo element in the real status bar">

## ✨ What it does

* **One icon instead of three.** Battery, Wi-Fi and cellular become a single ring — clean and calm.
* **The percentage lives inside the ring**, so you get the number *and* the shape at a glance.
* **It changes colour for you:** green while charging, yellow in power saver, red under 20 %.
* **Real signal at a glance:** Wi-Fi arcs light up as the signal grows, four spheres show your bars.
* **A charging story:** plug in and the lightning bolt rises from the middle of the ring into the top gap.
* **Airplane, Do Not Disturb and 5G** slide into the middle — and back out — with a soft morph.
* **Make it yours:** size, position, animation speed, and which animations you want (or none at all).
* **Tap it (optional):** hand taps to the [Auto Expand](https://github.com/kvmy666/AutoExpandNotifications)
  module to toggle Wi-Fi, Do Not Disturb, airplane mode or power saving.

## 🎬 See it in the app

Every animation has a live demo right next to its switch, so you can see exactly what you are turning on or off:

<img src="https://cdn.jsdelivr.net/gh/kvmy666/duoStatusBar@main/docs/media/app-animations.png" width="300" alt="The Animations section with live demos for Appear, Disappear and Charging">

## 📲 Install (about two minutes)

1. Download the APK from **[Releases](https://github.com/kvmy666/duoStatusBar/releases)** and install it.
2. Open **LSPosed → Modules**, enable **Duo Status Bar**, and tick **System UI** in its scope.
3. **Restart System UI** (or just reboot).
4. Open the **Duo Status Bar** app and flip the master switch on.

That's it. The module is **off until you switch it on**, so nothing changes until *you* say so.

## ✅ What you need

* Android **15 or newer** on a custom ROM, rooted with **LSPosed**.
* Tested on **OnePlus 15 / OxygenOS 16 (Android 16)** with KernelSU + LSPosed 2.2.0.
* Other ROMs are welcome — if something looks off, tell me and I'll add support.

## 🛟 Safe by design

* **Off means off.** With the default settings the module hooks nothing, hides nothing, and doesn't even
  swallow a tap.
* **Your icons come back.** The stock icons are only *hidden*, and their original look is remembered — turn
  the module off and they return exactly as they were.
* **It can't crash-loop your phone.** If the graphics ever fail twice, the module quietly falls back to a
  simple drawing instead of trying again.
* **A kill switch that always works**, even if the app won't open:

  ```powershell
  adb shell settings put global duo_statusbar_stage 0   # off
  adb shell settings put global duo_statusbar_stage 1   # simple drawing, no native code
  adb shell settings put global duo_statusbar_stage 2   # full animation
  ```

## 🎛️ Make it yours

Open the app and you'll find:

| Section | What you can do |
|---|---|
| **Battery icon** | Turn it on, show or hide the percentage, change the **size**, drag the **position**, and choose whether changes apply **live** or after a restart |
| **Animations** | A master switch, an animation **speed**, and separate toggles for **Appear**, **Disappear** and **Charging** |
| **Appearance** | Use **smooth graphics** (turn off if your phone ever feels slow), and draw the status-bar **clock in the system font** so it matches the ring |
| **Tap actions** | Choose what a single tap, double tap and long press do (with Auto Expand) |
| **About** | See the module's status, share a report, or support the developer |

<img src="https://cdn.jsdelivr.net/gh/kvmy666/duoStatusBar@main/docs/media/app.png" width="300" alt="The Duo Status Bar settings screen">

Changing the **size** asks for a restart (there's a **Restart System UI** button right there) — it's the one
setting that can't safely change while the bar is running.

## 👆 Tap actions (optional)

Taps on the element are handled by my other module,
**[Auto Expand](https://github.com/kvmy666/AutoExpandNotifications)**, which owns the actions. This keeps
things simple and safe: **Duo draws, Auto Expand acts.** With the default "No Action", the element doesn't
consume a single touch — so your usual status bar gestures keep working untouched.

## ❓ Questions people ask

**Will this slow down my phone?**
No. It's one small drawing in the status bar. If you ever want zero animation, the Animations master switch
turns it all off.

**Do I lose my battery percentage?**
Never — you can show it inside the ring, or hide it and keep the shape.

**What if I don't like it?**
Flip the master switch off, or run the kill switch above. Your stock status bar comes right back.

**Does it work on my phone?**
It's made for custom-ROM Android 15+ with LSPosed. If it isn't tested on your device yet, try it — and if
something looks wrong, send me a report.

## 🐞 Bugs and feedback

* **Issues:** https://github.com/kvmy666/duoStatusBar/issues — a log is worth more than a description.
  You can share one straight from the app's **About** section.
* **Telegram:** [@kvmy1](https://t.me/kvmy1)

## 💜 Support

If Duo Status Bar makes you smile every time you glance at your phone:
[Buy Me a Coffee](https://www.buymeacoffee.com/kroomfahd) or [PayPal](https://paypal.me/kroomfahd).
Thank you. 💜

## Credits

* The element's geometry was informed by [`lingyired/status-trio`](https://github.com/lingyired/status-trio)
  and the author's own screenshots. What was reused and what was not is written down in
  `docs/references.md`.
* Built on [Rive](https://rive.app), [LSPosed](https://github.com/LSPosed/LSPosed) and AndroidX / Compose.

## License

GPL-3.0 — see [LICENSE](LICENSE).
