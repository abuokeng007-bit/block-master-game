# Android build using GitHub Actions (no PC required after upload)

This starter source has not been compiled in this workspace because the Flutter SDK and Android SDK are not installed here. Use GitHub's hosted build runner:

1. Create a GitHub account and a new **private** repository named `block-master`.
2. Upload the contents of this ZIP into the repository root (not the ZIP file itself). Keep `.github/workflows/android-build.yml`; if the phone upload UI hides dot-folders, create the workflow file in GitHub's web editor at that exact path.
3. Commit the files to the `main` branch.
4. Open the repository's **Actions** tab. Select **Build Android APK and AAB**, then choose **Run workflow** if it did not start automatically.
5. Wait for the workflow to finish successfully.
6. Open the completed run and download the artifact named `block-master-android-builds`.
7. Extract it. It contains `app-release.apk` for device testing and `app-release.aab` for Google Play submission.

Important:
- The workflow generates the standard Android project files and builds both formats.
- The resulting release build is not yet signed with your own Play upload key. Before publishing to Google Play, configure a private upload keystore and Gradle signing; never share its passwords or key.
- Change the Android application ID to a unique ID you own before publishing. The workflow currently uses Flutter's generated default application ID, so do not submit it unchanged.
- This is a newly written starter game, not the original vendor source.
