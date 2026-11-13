# Changelog

## Ringlet 2.1 (build 4)

### New
- When an update is out, a banner at the top of the panel says so. Click it to download.
- Ringlet checks for updates every few hours and when your Mac wakes up, not just once a day.

### Fixed
- The update check now reads from the Ringlet releases page on GitHub.

## Ringlet 2.0 (build 3)

DuoBar is now **Ringlet**. Your license key and settings carry over. Quit DuoBar and drag it to the Trash before installing.

### New
- **Unfold.** Hover over the icon (or click it, your choice) and the ring spins open into separate battery, Wi-Fi, network and sound icons. Click one to open its page right under it.
- **Moments.** The icon plays a short animation when something changes, then goes back to normal: Focus on and off, charger in and out, mute, volume, network lost and back, AirPods connecting, low battery and drives plugging in.
- **Stats panel.** Pages for Wi-Fi (nearby networks, join saved ones), Bluetooth (devices with battery levels, connect and disconnect), Sound (output picker, mic mute), Battery (health, cycle count, Low Power Mode), Network, CPU and Memory (live graphs and top apps) and Disk (free space, eject).
- **Make it yours.** Put any of 8 readings in the ring, center or dots. Three ring styles (solid, gradient, segmented), nine colors and three profiles: Desk, On the Go and Quiet.
- **Settings window.** A real window with General, Icon, Moments and License tabs. It stays open when you click into other apps.
- **Brightness slider** and a **Bluetooth on/off switch** in the panel.
- **Updates.** Ringlet now checks for new versions and shows a Download button in Settings > License.

### Fixed
- Battery health now matches System Settings. The measured capacity in mAh is shown under it.
- Network dots now follow your actual traffic: one dot when idle, full while downloading.
- The center showed the Ethernet icon while on Wi-Fi.
- The volume slider in the panel lagged.
- The Wi-Fi icon flickered when the signal sat between two bars.

### Performance
- About 0% CPU when idle and around 15 MB of memory. The panel and Settings window use nothing once closed.

### Installing
This build isn't notarized by Apple yet. After dragging Ringlet to Applications, run this once in Terminal:

```
xattr -dr com.apple.quarantine /Applications/Ringlet.app
```

## DuoBar 1.1 (build 2)
- First tester build: battery ring, Wi-Fi glyph and volume dots in one icon, click to expand, license keys and a 14-day trial.
