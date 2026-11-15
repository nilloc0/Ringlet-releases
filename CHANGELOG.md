# Changelog

## Ringlet 3.2 (build 10)

### New
- **Charge to Full Now.** When macOS is holding your battery at 80% (Optimized Battery Charging or a Charge Limit), the Battery page and the right-click menu show a Charge to Full Now button. It's Apple's own override, so it lasts until you unplug and doesn't change your settings. No need to keep Apple's battery icon around just for this.

### Improved
- **A simpler right-click menu.** It's down to quick actions: volume and brightness sliders, switch profiles, mute sound or the microphone, open Settings, quit. Wi-Fi and outputs are in the panel (left click), and everything else (icon size, fold delay, hover, alerts, moments, license, updates, troubleshooting) is in the Settings window.
- The Welcome Tour moved to Settings > General.

## Ringlet 3.1 (build 9)

### New
- **Make the profiles your own.** Desk, On the Go and Quiet are now yours to set up. Pick a profile in Settings > Icon and change the ring, center, dots, color or ring style: the changes save to that profile, so it comes back exactly that way next time, whether you pick it or automatic profiles switch to it. A Reset button puts any profile back to how it shipped.
- If you had a custom setup from an older version, a Save as menu lets you keep it as one of the three profiles.

### Improved
- The last DuoBar names are gone: Ringlet's logs and support files now live in folders named Ringlet. They move over by themselves the first time 3.1 opens.

## Ringlet 3.0 (build 8)

The biggest update since the first release. Ringlet now adapts to where you are, shows more of what's going on inside your Mac, and the whole app got a polish pass.

### New
- **Automatic profiles.** Turn it on in Settings > Icon and Ringlet switches to Desk when you plug into a display or Ethernet, On the Go when you leave, and Quiet during a Focus. Pick a profile yourself and it sticks until your setup changes. The new profile swipes through the middle of the ring when it switches.
- **Live power draw.** The Battery page shows how many watts your Mac is using, what the charger is delivering, and how fast the battery is charging or draining.
- **Running Hot moment.** When macOS starts slowing your Mac down to cool it, a flame rises through the ring. A snowflake shows when it cools off. The CPU page shows the current heat level too.
- **Accessory battery alerts.** Get a notification when AirPods, a keyboard or a mouse drops to 20% and again at 10%. On by default, with a switch in Settings > General.
- **Welcome window.** New installs get a quick setup: Wi-Fi names, hiding Apple's duplicate icons, automatic profiles and open at login. Open it any time from the right-click menu (Welcome Tour).
- **App icon.** Ringlet has its own icon: the ring on dark glass. It shows in Finder, Launchpad, Settings and on the installer disk.

### Improved
- **Wi-Fi names.** The Wi-Fi page and Settings > General explain why macOS needs Location access to show your network name, with an Allow button. Ringlet no longer asks out of nowhere at launch.
- **Centered moments.** Every symbol in a moment (Focus, AirPods, drives, mute and the rest) now sits dead center in the ring.
- **Device icons.** iPhone, iPad, Apple Watch, Mac and Apple Pencil get their own icons in Bluetooth, and renamed AirPods are recognized. Sound outputs show what they are: built-in speakers, a display, AirPlay, Bluetooth or USB.
- **Sound outputs update instantly** when you plug something in, and hidden virtual devices from meeting apps are left out of the list.
- **Top apps.** The busiest apps on the CPU and Memory pages are grouped by name, so a browser's helper processes count as one app.
- **Calmer network moments.** Waking from sleep or switching networks no longer plays Network Lost and Back. Ringlet waits a few seconds before calling the connection lost, and only says Back if it said Lost.
- **Lighter on your Mac.** Ringlet checks the Wi-Fi name every 15 seconds instead of every second, and still idles under 1% CPU with about 14 MB of memory.

### Fixed
- The icon could be drawn taller than the menu bar on some screens. It now sizes itself to the bar.
- AirPods battery levels now show in the panel and in the headphones moment.
- Mounting a disk image (an installer, or Ringlet's own update) no longer plays the drive moment.
- A Focus whose symbol macOS doesn't share now shows the moon instead of nothing.
- "This Session" network totals could be up to three times too high. They now count real bytes.
- Scrolling on the icon to change the volume went the wrong way with natural scrolling. Fingers up is now always louder.
- The Wi-Fi page showed your Ethernet IP address when docked. It now shows the Wi-Fi address.
- With Location off, the Wi-Fi page said "No other networks found" when macOS was just hiding them. It now tells you to allow Location.
- Disconnected Bluetooth devices no longer show an old battery level.
- Speeds and sizes said "Zero KB" instead of "0 KB".
- The Low Power Mode and Mute Microphone switches now line up with every other switch.
- The bottom of Settings > General was cut off.
- If Ringlet launched while offline, it waited six hours to check for updates again. It now retries at the next check.
- The Buy button pointed at the wrong website.

## Ringlet 2.3 (build 6)

### Fixed
- Settings showed the wrong choices for the ring, center and dots (for example "Battery" while the ring was showing memory). They now always match the icon and update the moment anything changes.
- The selected profile and color stayed highlighted after picking a different one.

## Ringlet 2.2 (build 5)

### New
- **Updates install themselves.** When a new version is out, click Install in the panel, the right-click menu or Settings > License. Ringlet downloads it, checks it's genuine, swaps itself out and restarts. No browser, no DMG, no Terminal command.
- Every update is signed. If a download doesn't match what was published, Ringlet refuses to install it.

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
