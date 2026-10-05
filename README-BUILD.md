# Informatica Android — Cloud Build

This package is prepared for a GitHub Actions cloud build.

## Tablet-only build steps

1. Create a GitHub repository.
2. Upload the CONTENTS of this folder to the repository root.
   Make sure `.github/workflows/build-apk.yml` is included.
3. Open the repository's **Actions** tab.
4. Select **Build Informatica APK**.
5. Choose **Run workflow**.
6. Wait for the workflow to finish.
7. Open the completed workflow run and download the artifact
   named **Informatica-debug-apk**.
8. Extract the downloaded artifact and install `app-debug.apk`
   on your Android device.

The workflow uses a GitHub-hosted Ubuntu runner, JDK 17, Android SDK
platform 36/build-tools 36.0.0, and Gradle Wrapper.

## Important

- This produces a real Android debug APK.
- The debug APK is for personal/testing installation.
- External AI providers, Wikipedia, remote fonts/images, etc. still
  require internet access at runtime.
- Do not upload signing passwords or private keys into the repository.
