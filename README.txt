KenseiTune app package
======================
This is an installable web app (PWA). Host it on HTTPS before using Spotify sign-in or installing it.

HOST THE APP
------------
1) Upload the whole kenseitune-app folder to Netlify Drop, or publish it with GitHub Pages.
2) Open the HTTPS website on your phone or computer.
3) Android: Chrome menu > Install app. iPhone/iPad: Safari Share > Add to Home Screen.

CONNECT SPOTIFY
---------------
1) Create an app in the Spotify Developer Dashboard.
2) In KenseiTune, open Settings > Music Services and copy the Redirect address shown there.
3) Add that exact address to your Spotify app's Redirect URIs.
4) Paste the Spotify Client ID into KenseiTune, press Save service settings, then Connect Spotify.
5) Approve access. Spotify search results open in Spotify's official embedded player.

Spotify uses Authorization Code with PKCE. Do not add a Spotify client secret to this static website. The embedded player uses Spotify's own controls; KenseiTune's local audio effects and transport controls do not control Spotify playback. Spotify playback availability and account requirements are controlled by Spotify.

CONNECT YOUTUBE MUSIC / YOUTUBE
-------------------------------
1) For in-app search, create a YouTube Data API v3 key in Google Cloud and restrict it to your hosted website.
2) Paste the key in Settings > Music Services and save.
3) Search for a song in Search, then choose a result. You can also paste a YouTube or YouTube Music video URL without an API key.
4) Playback uses the official YouTube embedded player and its controls.

The YouTube API key is stored in this browser on this device. Restrict the key by website referrer and API. Never publish an unrestricted key.

NOTES
-----
- Spotify and YouTube playback are provided by their official embedded players. The existing KenseiTune demo player, lyrics, themes, library, and other local features remain available.
- External music players need an internet connection and may not work offline.
- Music availability, ads, playback restrictions, and account requirements are controlled by the respective services.
- If the app was already installed, close and reopen it after updating so the new service worker cache can activate.
- Settings, your photo background, and lyrics you add stay on that device.
