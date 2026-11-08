# Bali Mobile Lab

Personal, free, mobile-friendly GitHub project workspace published as a static GitHub Pages site.

## Features
- Browse public GitHub repositories, branches, folders, and files.
- Preview standalone HTML files in a sandboxed iframe.
- Inspect an APK selected from the phone: filename, size, and SHA-256. The APK is processed locally and is not uploaded.
- Run the included GitHub Actions workflow to build a debug APK from a selected public Android Gradle repository.

## Limitations
- Static browser app: no backend, paid API, cloud emulator, or Android virtual device.
- Native APK files cannot execute in this browser workspace.
- Standalone HTML preview is not a framework build. React, Vue, Vite, and similar projects require their own build/hosting environment.
- Public repositories only; GitHub unauthenticated API rate limits apply.

## Publish using GitHub Pages
Open Settings > Pages. Select Deploy from a branch, choose main and /(root), then Save. Wait for the Pages URL to appear in Settings > Pages.

## Build an Android APK
1. Open Actions > Build Android APK > Run workflow in this repository.
2. Enter the public Android project repository as owner/name, for example owner/project, and its branch or tag.
3. Run the workflow and wait for completion.
4. Download the debug-apk artifact from the completed run.

The selected project must have a Gradle wrapper at its root and an Android application module that supports assembleDebug. Private repositories and projects requiring extra secrets or custom build steps are not supported by this simple workflow.

## Privacy
Repository browsing uses public GitHub API endpoints. APK file inspection is local to the browser tab; no APK upload endpoint exists.
