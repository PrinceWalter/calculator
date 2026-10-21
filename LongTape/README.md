# Long Tape Calculator for Android

A phone calculator with live results, smart brackets, a scientific panel, and a history that keeps every calculation with no limit. History is saved on the phone and survives app updates.

## Get the APK without installing anything (GitHub builds it for you)

1. Sign in at github.com (a free account is fine) and create a new **public** repository, for example `long-tape-calculator`.
2. Upload everything in this folder to the repository, including the hidden `.github` folder. On a computer: unzip, then drag the folder's contents onto the repository's "uploading an existing file" page.
3. Open the repository's **Actions** tab. A build named "Build APK" starts on its own and takes about 3–5 minutes.
4. When it finishes, open **Releases** on the repository's main page and tap `LongTape.apk` on your phone.
5. Android will ask to allow installing apps from your browser. Allow it, then tap **Install**.

Your permanent download link is:
`https://github.com/<your-username>/<repo-name>/releases/latest/download/LongTape.apk`

Every time you change a file and save it to the `main` branch, GitHub builds a new version. Install it over the old one and your history stays.

## Build it on a computer instead

Open this folder in Android Studio, wait for it to finish syncing, then choose **Build › Build APK(s)**. Or from a terminal: `./gradlew assembleRelease`. The APK appears in `app/build/outputs/apk/release/`.

## What's inside

- `app/src/main/assets/index.html` — the calculator itself. Edit this to change how it looks or works.
- `app/src/main/assets/fonts/` — fonts bundled so the app works fully offline.
- `app/src/main/java/.../MainActivity.kt` — the Android shell: shows the calculator, handles the back button, copying results, and light/dark mode.
- `app/longtape.keystore` — the app's signing key. Keep it; updates must be signed with the same key or Android will refuse to install them over the old app.

## About the history

- There is no cap on how many calculations are saved.
- It lives in the app's private storage. Uninstalling the app or using "Clear storage" in Android settings deletes it. Updating the app does not.
