# Bali Mobile Lab

Personal, free, mobile-friendly GitHub project workspace published as a static GitHub Pages site.

## Features
- Browse public GitHub repositories, branches, folders, and files.
- Preview standalone HTML files in a sandboxed iframe.
- Inspect an APK selected from the phone: filename, size, and SHA-256. The APK is processed locally and is not uploaded.
- Includes a GitHub Actions workflow template for building a debug APK from a conventional Android Gradle project.

## Limitations
- Static browser app: no backend, paid API, cloud emulator, or Android virtual device.
- Native APK files cannot execute in this browser workspace.
- Standalone HTML preview is not a framework build. React, Vue, Vite, and similar projects require their own build/hosting environment.
- Public repositories only; GitHub unauthenticated API rate limits apply.

## Publish using GitHub Pages
Open Settings > Pages. Select Deploy from a branch, choose main and /(root), then Save. Wait for the Pages URL to appear in Settings > Pages.

## Android APK workflow template
Copy .github/workflows/android-apk.yml into the Android Gradle project repository. Open Actions > Build Android APK > Run workflow. Download the debug-apk artifact from the completed run. This expects a Gradle wrapper at repository root and an Android application module that supports assembleDebug.
