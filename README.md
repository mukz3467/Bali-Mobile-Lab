# Bali Mobile Lab

Personal Android app testing workspace for the Noor-e-Hidayat project.

## What this workspace does
- Provides a mobile-friendly testing dashboard; source code is hidden from the main interface.
- Builds a real Android debug APK from the public GitHub repository `mukz3467/Noor-e-hidayat-2`.
- Shows the latest GitHub Actions build status.
- Provides a phone-side checklist for testing real app features.
- Lets you inspect the APK filename, size, and SHA-256 locally in the browser.

## Build and test Noor-e-Hidayat
1. Open the dashboard and tap **Build latest Noor-e-Hidayat APK**.
2. In GitHub Actions, choose **Run workflow**. The repository and `main` branch are pre-filled.
3. Wait for the workflow to finish. Open the successful run and download the `debug-apk` artifact.
4. Extract the ZIP, install the APK on your Android phone, and test the actual native app.

## Important limitation
This static GitHub Pages dashboard is not an Android emulator and does not execute APKs in the browser. Real native app testing happens after installing the built APK on an Android device. No fake phone frame or website iframe is presented as a native app preview.

## Build requirements
The workflow uses Java 17 and Gradle 9.3.1, then runs `gradle assembleDebug`. It is configured for the public Noor-e-Hidayat repository by default. GitHub Actions usage is subject to GitHub account limits.

## Publish
Open repository Settings > Pages. Choose **Deploy from a branch**, branch `main`, folder `/(root)`, then Save. Use the Pages URL displayed by GitHub after deployment completes.
