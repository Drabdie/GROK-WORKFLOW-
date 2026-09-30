# NEXUS GameSpace build preparation

This archive now contains Android Gradle project configuration and a GitHub Actions workflow.

## Build APK
- GitHub: add the project contents to a repository, then open Actions → Android APK → Run workflow. Download artifact `NEXUS-GameSpace-debug-apk` after the run succeeds.
- AndroidIDE: open this project folder (the folder containing `settings.gradle`), sync Gradle, then run `:app:assembleDebug`.

## Important
- This is a debug APK build setup, not a signed release APK.
- Hardware tuning, accurate FPS/temperature readings, and killing other apps are limited by Android/OEM permissions and root availability.
- The project has not been compiled in this environment because Android SDK and Gradle are not installed here. A successful CI/AndroidIDE build is still required before calling the APK verified.
