# Block Master — Flutter source project

This is a newly written, clean-room block puzzle implementation based on the general block-placement puzzle genre. It is **not** the original source code extracted from the supplied APK and does not include the original developer's artwork, branding, or proprietary assets.

## Included features
- 10×10 board
- Three selectable pieces per round
- Tap a board cell to place the selected piece
- Full row and column clearing
- Score and in-session best score
- Basic no-move/game-over detection
- Restart button
- Responsive Material UI

## Requirements
- Flutter SDK (stable)
- Android Studio or Flutter-compatible development environment
- Android SDK

## Run
```bash
flutter pub get
flutter run
```

## Build for Google Play
```bash
flutter build appbundle --release
```
The output is normally:
`build/app/outputs/bundle/release/app-release.aab`

Before publishing:
1. Change `applicationId` in `android/app/build.gradle` or `android/app/build.gradle.kts` to a unique ID you own.
2. Set your app name, icon, version and signing configuration.
3. Test on multiple Android devices and screen sizes.
4. Add a privacy policy if the app collects personal data or uses advertising/analytics SDKs.
5. Add and test AdMob only after creating your own AdMob account and app/ad units.
6. Complete the Google Play Console Data safety, content rating, target audience and store listing forms accurately.
7. Check current Google Play target API and testing requirements before release.

## Current limitations
- No drag-and-drop placement yet; select a piece then tap its top-left board cell.
- No persistent high score, sound, haptics, online leaderboard, cloud save or ads.
- This is a starter source project and must be built and tested before release.

## Project structure
- `lib/main.dart` — game UI, board state, placement, clearing and scoring
- `pubspec.yaml` — Flutter project configuration
- `docs/PROJECT_GUIDE.md` — implementation and release notes
