ISLAND HOP - Android app (Capacitor)

The game is www/index.html. Data is kept in users.json inside the app's private storage:
read at start, saved after every answer/game, and when the app goes to the background.

=== Way 1: no Android Studio, build in the cloud (free) ===
1. Create a GitHub account and a new empty repository.
2. Upload everything in this folder, INCLUDING the hidden ".github" folder.
   (Easiest: install GitHub Desktop, "Add local repository", Commit, Publish.)
3. On GitHub open the "Actions" tab > "Build Android APK" > "Run workflow".
4. After ~5 minutes open the finished run and download the artifact "island-hop-apk".
   Unzip it: app-debug.apk is the app.
5. Copy app-debug.apk to the phone, open it, allow "Install unknown apps" when asked.

=== Way 2: on your computer (needs Node.js LTS + Android Studio) ===
  npm install
  npx cap add android
  npx cap sync android
  npx cap open android      (then press Run with the phone connected by USB)

For Google Play you need a signed release build and a developer account ($25 once).
