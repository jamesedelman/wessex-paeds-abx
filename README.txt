WESSEX PAEDIATRIC EMPIRICAL ANTIMICROBIAL PRESCRIBING GUIDANCE
Offline-capable, installable web app (PWA)
================================================================

WHAT'S IN THIS FOLDER
  index.html              The full guide (self-contained, ~2.8 MB)
  manifest.webmanifest    App metadata (name, icon, colours)
  sw.js                   Service worker (enables full offline use)
  favicon.ico             Browser tab icon
  icons/                  App icons (home-screen / desktop)

----------------------------------------------------------------
TWO WAYS TO USE IT
----------------------------------------------------------------

1) QUICK / NO SERVER (works offline, but NOT installable)
   Just open index.html in any browser. Because everything is
   embedded in the single file, it already works with no internet
   connection. You can also email it or put it on a shared drive.
   (Home-screen install and the app icon are NOT available this way -
   browsers block that for files opened directly from disk.)

2) FULL APP - OFFLINE + INSTALLABLE WITH ICON  (recommended)
   The home-screen install + distinctive icon require the files to be
   served over https from a web address. Host this whole folder on any
   web server / intranet / static host (e.g. SharePoint hosting, GitHub
   Pages, Netlify, an NHS intranet site, or a trust web team).

   Once it's live at an https:// address:

   On iPhone / iPad (Safari):
     - Open the address in Safari
     - Tap the Share button, then "Add to Home Screen"
     - The Wessex icon appears on the home screen; opens full-screen
       and works offline afterwards.

   On Android (Chrome):
     - Open the address in Chrome
     - Tap the menu (three dots), then "Install app" / "Add to Home screen"

   On Windows / Mac (Chrome or Edge):
     - Open the address
     - Click the install icon in the address bar (or menu > "Install...")
     - It installs as a desktop app with its own icon.

   The first visit caches everything; after that it opens and runs
   with no internet connection.

----------------------------------------------------------------
UPDATING THE CONTENT
----------------------------------------------------------------
   When you publish a new version, edit the CACHE version string near
   the top of sw.js (e.g. change "...-v1" to "...-v2"). That tells
   installed copies to refresh their cached files on next launch.
