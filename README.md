# Duo Status Bar

[![Downloads](https://img.shields.io/github/downloads/kvmy666/duoStatusBar/total?label=downloads)](https://github.com/kvmy666/duoStatusBar/releases)
[![Latest release](https://img.shields.io/github/v/release/kvmy666/duoStatusBar)](https://github.com/kvmy666/duoStatusBar/releases)
[![Android 13+](https://img.shields.io/badge/Android-13%2B-3ddc84)](https://developer.android.com)

Duo Status Bar replaces the battery, Wi-Fi and mobile signal icons in your status bar with one clean,
animated indicator.

It is an LSPosed module. It does not modify system files. It only hides the icons it replaces and draws
the new indicator. You can turn it off at any time, and your original icons come back exactly as they
were.

<p align="center">
  <img src="https://cdn.jsdelivr.net/gh/kvmy666/duoStatusBar@main/docs/media/status-bar.png" width="360" alt="Duo Status Bar in the status bar">
</p>

## Requirements

- Android 13 or newer.
- A custom ROM with root.
- LSPosed installed.

## Install

1. Download the APK from [Releases](https://github.com/kvmy666/duoStatusBar/releases) and install it.
2. Open LSPosed, go to Modules, and enable Duo Status Bar.
3. In the module's scope, tick **System UI**.
4. Restart System UI, or reboot the phone.
5. Open the Duo Status Bar app and turn the main switch on.

The module is off until you turn it on. Nothing changes before that.

## Settings

- **Battery icon** - show or hide the percentage, change the size, and move the position.
- **Animations** - turn animations on or off, and set the speed.
- **Appearance** - icon colour, smooth graphics, the clock font, and what appears in the middle.
- **Status bar icons** - keep your other icons visible beside the indicator, or hide them.
- **Tap actions** - optional. Handled by the Auto Expand module.
- **About** - see the module status and send a report.

Changing the size needs a System UI restart. The app has a button for it.

## Turn it off

Use the switch in the app, or run one of these commands:

```text
adb shell settings put global duo_statusbar_stage 0   # off
adb shell settings put global duo_statusbar_stage 1   # simple drawing, no native code
adb shell settings put global duo_statusbar_stage 2   # full animation
```

## If something goes wrong

- Issues: https://github.com/kvmy666/duoStatusBar/issues
- Telegram: https://t.me/kvmy1

Send a report from the app's **About** section. It includes your device details and the logs, which
makes the problem much easier to find.

## Support

If you like the app, you can support the developer:
[Buy Me a Coffee](https://www.buymeacoffee.com/kroomfahd) or [PayPal](https://paypal.me/kroomfahd).

## License

GPL-3.0. See [LICENSE](LICENSE).
