# THE FORCE WITHIN

An offline-first awareness and discipline app built as a web experience and packaged as a native Android WebView app.

## What this repo contains

- `index.html`: the full web app, including the intro flow, dashboard, training, reset, schedule, profile, and emotion log.
- `android/`: a native Android wrapper that loads the web app locally from `app/src/main/assets/index.html`.
- A launcher icon based on the Force symbol from the intro/philosophy artwork.

## What the Android app does

- Loads the app from local files instead of `localhost` or a remote server.
- Works offline once installed because the HTML is bundled into the APK assets.
- Keeps the full UI and local storage behavior of the web version.
- Uses the Force symbol as the app icon.

## How to use it

1. Open the `android/` folder in Android Studio.
2. Let Android Studio sync the Gradle project.
3. Run the `app` configuration on a device or emulator.
4. The app opens directly into the local WebView build.

If you want a release APK:

1. Open the `android/` project in Android Studio.
2. Build the `release` variant.
3. Use the generated APK from the `android/app/build/outputs/apk/` folder.

## Offline behavior

- The Android wrapper loads `file:///android_asset/index.html`.
- The web app no longer depends on external fonts for the Android build.
- All user state stays local to the device browser storage inside the WebView.

## Key app areas

- Intro and trainer name setup
- Core dashboard
- Morning training flow
- Evening reset flow
- Schedule builder
- Emotion tracker
- Profile, statistics, achievements, reports, and timeline

## Repository layout

- `index.html` - main web app
- `android/` - Android Studio project
- `android/app/src/main/assets/index.html` - packaged offline web app
- `android/app/src/main/res/` - Android resources and launcher icon

## Notes

- The Philosophy action appears once in the Profile action area.
- The app is designed to be used locally, without a hosted backend.
- JavaScript parsing and browser validation were checked after the latest UI and Android wrapper updates.
