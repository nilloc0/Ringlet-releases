# Building and shipping Ringlet

## Everyday builds

```
./build.sh
```

Builds a production copy of the next unreleased version (the version and build number in
`Info.plist`), puts it in /Applications and restarts it. The copy it replaces is moved to
`backups/` (only one backup is kept). If a build is broken, `./rollback.sh` swaps the backup
back in.

`./build.sh --dev` builds a separate copy with the developer test hooks (`--render`,
`--snapshot`, `--profile-test` and friends) into `build/dev/`. It never installs anything.

## Releasing

```
./release.sh 3.1 "Short line shown in the in-app update banner."
```

Builds the DMG into ~/Downloads and writes a signed `appcast.json`. Then:

1. GitHub > Releases > Draft a new release, tag `v3.1`, attach the DMG, paste the notes, publish.
2. Upload the new `appcast.json` to the repo. Do this last: it's what tells everyone's app
   the update exists.

After a release, `release.sh` moves `Info.plist` on to the next build number so the next
`./build.sh` is the following unreleased version.

## Issuing keys

The signing key lives at `~/.ringlet/private.key`. **Keep a copy somewhere off this Mac.**
If you lose it you can't issue license keys or sign updates that existing copies accept.
If someone else gets it, they can do both.

```
./build/keygen issue --name "Jax" --type D --days 90    # a tester, expires in 90 days
./build/keygen issue --name "jane@email.com"            # a sale, never expires
./build/keygen check <key>                              # read a key back
./build/keygen list                                     # everything issued so far
```

Types: `S` standard (a sale), `D` developer (a tester), `F` founder (yours).

## Names that still say DuoBar (on purpose)

The bundle ID `com.duobar.app` (which is also the settings domain), the keychain trial
record and the menu bar position key keep the old name. Changing them would wipe
everyone's settings, licenses, trial dates and icon position, and the updater only
installs builds with the same bundle ID.

## Before charging anyone

1. Apple Developer Program, $99/year, for Developer ID signing and notarization. Without it,
   macOS warns about an unidentified developer and asks for permissions again after updates.
   `build.sh` picks up a Developer ID certificate automatically once it's in your keychain.
2. A merchant of record (Paddle or Lemon Squeezy) so sales tax is their problem.
3. A real store page for the Buy button (`buyURL`).
