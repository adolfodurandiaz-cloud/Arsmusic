# Build armusic APK without Android Studio

This project includes a GitHub Actions workflow at `.github/workflows/build-apk.yml`. GitHub's cloud runner installs Java/Gradle and builds a debug APK, so Android Studio is not needed on your phone or computer.

## Steps (can be done from a phone)
1. Sign in or create an account at https://github.com.
2. Create a new repository, for example `armusic`.
3. Upload the *contents* of this project folder to the repository (including the hidden `.github` folder). Make sure `app/`, `build.gradle.kts`, and `settings.gradle.kts` are at the repository root, not nested in an extra `armusic/` folder.
4. Open the repository's **Actions** tab and select **Build armusic APK**.
5. Tap **Run workflow** if it has not run automatically after your upload.
6. When the run completes successfully, open it and download the `armusic-debug-apk` artifact.
7. Extract the downloaded artifact ZIP on your Android phone and tap `app-debug.apk` to install it. If Android asks, allow your browser or file manager to install unknown apps.

The APK generated this way is a debug build for testing, not a Play Store release. The first build can fail if source code needs fixes; check the workflow logs in that case. The build requires internet access on GitHub's runner, not on your phone during playback.
