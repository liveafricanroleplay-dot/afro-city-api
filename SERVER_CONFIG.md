# AFRO CITY RP server configuration

- Host: 142.132.203.47
- Port: 14585
- Android package: com.afrocityrp.launcher

The port is the one supplied by the server owner. A successful launcher build does not prove that the server is reachable or that the game client supports automatic connection. Verify those separately before advertising the connection feature as working.

Do not place database credentials or passwords in this Android app.

## News feed format
Set `newsUrl` in MainActivity.kt to an HTTPS endpoint returning:
`[{"title":"...","date":"2026-11-08","summary":"...","url":"https://..."}]`
Cleartext HTTP is blocked on purpose.

## Game files manifest
Set `filesManifestUrl` in MainActivity.kt to an HTTPS endpoint returning:
`[{"path":"models/skin1.dff","url":"https://...","sha256":"<64-char hex>","size":12345}]`
Every entry needs a sha256; files failing the check are discarded. Files save to the app's own
external folder (shown on the Game Files screen). Newer Android versions may stop other apps
(your game client) from reading that folder, so test with your client.

## Client detection
The launcher finds any installed app that handles `samp://` links. It does not name a specific client.
