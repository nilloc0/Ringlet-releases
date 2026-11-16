# Ringlet 3.5

## Ringlet on your lock screen (beta)

Lock your Mac and your ring is right there under the clock, with your battery status, your AirPods and keyboard levels, and how long you've been away. Moments play there too, so plugging in while locked makes the ring swell with a green glow.

- **Click the ring** and it rolls back to the middle and swallows everything. Click again and it rolls out, with your status beside it and the rest popping out underneath.
- **Charge to Full Now** shows up on the lock screen when your battery is on hold, for when you lock up and head out.
- **While you were away:** "Locked 2h 14m · used 6%", so you can tell if something drained your battery while you were gone.
- **Now Playing** for Apple Music and Spotify, with artwork, play/pause, skip and a progress bar. You can hide song names and artwork, or turn the player off completely.
- **Every display** gets its own ring, centered, even one that wakes up late or gets plugged in while you're locked.
- It gets out of the way while a screen saver is running.

It's built into Ringlet, so there's nothing extra to install. It never takes your typing away from the password field, and it's gone the moment you unlock. Turn it on in **Settings > General > Lock Screen**.

The first time you turn on the player, macOS asks to let Ringlet control Music or Spotify. Answer it while you're unlocked, since the lock screen can't show that prompt.

**The lock screen is still in beta.** If something looks off (a missing ring, a display without one, controls that don't respond), open an issue at [github.com/nilloc0/ringlet-releases/issues](https://github.com/nilloc0/ringlet-releases/issues) or comment on one that's already there. A photo of your screen and the report from Settings > License > Copy Report help a lot.

## Charge to Full Now respects your Charge Limit

If you capped charging in System Settings > Battery (say, at 95%), Charge to Full Now charges to 95%, not 100%. Once you're there the button greys out and the status reads "Charged to your 95% limit" ("Charge limit reached" on the lock screen).

## OLED Care

A new setting in Settings > General slowly moves the lock screen ring a few points every few minutes, so nothing sits in one spot all night. It's off by default.

## Liquid Glass

On macOS 26 and later, the panel's cards and profile buttons are Liquid Glass, tinted with your ring's color. The Glass tint slider in Settings > Icon goes from clear to tinted, and each profile keeps its own tint, so the glass changes when you plug into a display or leave.

## Sharper icons

When the ring unfolds, the battery is drawn at its real level, glows green on power and shows a bolt while charging. Volume shows its percentage, and headphones show which ones you're using in blue. Ethernet has its own icon now, and CPU, memory and disk stay gray until they're worth noticing.

## How to update

On Ringlet 2.2 or newer: click **Install** in the update banner or in Settings > License. Ringlet downloads the update, checks that it's genuine, and restarts itself.

On an older version: download **Ringlet-3.5.dmg** below, open it, and drag Ringlet to Applications.

**Heads up:** after updating, macOS may ask again for Bluetooth, Location and Focus access. Click Allow and you're set.

Requires macOS 14 or later on Apple Silicon. Liquid Glass needs macOS 26 or later.
