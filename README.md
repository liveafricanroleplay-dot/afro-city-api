# AFRO CITY RP Android Launcher

Android Studio project for the AFRO CITY RP launcher.

## Confirmed server
- Address: 142.132.203.47
- Port: 14585
- Package: com.afrocityrp.launcher

## Current scope
- Branded Android launcher screen
- Copy server address action
- Discord link
- Live server status (SA-MP UDP query: players, ping, password flag)
- News feed from an HTTPS JSON endpoint (`newsUrl` in MainActivity.kt)
- Settings: saved player nickname, status auto-check toggle
- Explicit notice that account login is not connected yet
- GitHub Actions workflow to build a debug APK

## Important limitations
This app is a launcher, not a multiplayer game client. The "Open Multiplayer Client" button currently gives instructions rather than launching a client, because the exact compatible client's Android package and connection intent have not been verified. Account sign-in is not implemented and must not collect real passwords until a secure HTTPS authentication API is deployed.

No GTA: San Andreas game files are included.

## Build
Open the Actions tab and run **Build AFRO CITY RP Launcher APK**. On success, download the `afro-city-rp-launcher-debug-apk` artifact. The APK has not been claimed as tested until a workflow run succeeds.

<!-- Cloud build workflow is configured at .github/workflows/android-build.yml -->
