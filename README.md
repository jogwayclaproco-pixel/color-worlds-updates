# Color Worlds — Live Update Releases

This public repository hosts **web-only live update bundles** for the Color Worlds Android app.

- The game source repository remains private.
- Only production web assets (HTML, CSS, JavaScript, images) and release metadata belong here.
- Never upload source archives, signing private keys, credentials, or Android APK/AAB files here.
- Native Android changes and Capacitor plugin changes must be distributed through Google Play or a new APK.

## Release layout

Each release should publish:
- `version.json` — current bundle ID, minimum native app version, release notes, and ZIP URL.
- `bundles/<bundle-id>.zip` — the built web bundle, containing the contents of Vite's `dist/` directory.

The app must verify the bundle's SHA-256 checksum and RSA signature before activation. The RSA private key must be stored only as a GitHub Actions secret in the private game repository; the matching public key is embedded in the app.

No live update is active until the Live Update plugin and the app-side update checker have been integrated and tested in a new Android build.
