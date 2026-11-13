# Giving DuoBar to other people

## Issuing keys

The private key lives at `~/.duobar/private.key`. **Back it up now.** If you lose it you
cannot issue keys that existing copies of the app accept, and if someone else gets it they
can mint free keys forever.

```
./build/keygen issue --name "Jax" --type D --days 90    # a tester, expires in 90 days
./build/keygen issue --name "jane@email.com"            # a sale, never expires
./build/keygen check <key>                              # read a key back
```

Types: `S` standard (a sale), `D` developer (a tester), `F` founder (yours).
Leave `--days` off for a key that never expires.

## Sending a build to testers

```
./release.sh 1.1 "Fixed the size slider."
```

That bumps the build number, rebuilds, zips the app, and prints the JSON to publish.
Upload the zip somewhere public, then put that JSON at the URL in `Updates.feedURL`.
GitHub Releases works and costs nothing.

While testing you can point the app anywhere:

```
defaults write com.duobar.app updateFeed "https://raw.githubusercontent.com/<you>/duobar/main/appcast.json"
```

The app checks once a day and on launch. If the `build` number in the JSON is higher than
the running one, it posts a notification and adds a download row to the menu. It does not
install anything by itself, so a bad release can never break someone's copy.

## The Gatekeeper problem

Until the app is signed with a Developer ID certificate and notarized (which needs the
$99/year Apple Developer Program), macOS will refuse to open it on anyone else's Mac.

For friends testing, tell them to run this once after unzipping:

```
xattr -dr com.apple.quarantine /Applications/DuoBar.app
```

That is fine between friends who trust you. It is **not** acceptable to ask paying
customers to do it, so notarization has to happen before you sell a single copy.

## Before charging anyone

1. Apple Developer Program, $99/year, for Developer ID signing and notarization
2. A merchant of record (Paddle or Lemon Squeezy) so sales tax and VAT are their problem
3. Set `buyURL` and `updateFeed` to real addresses
