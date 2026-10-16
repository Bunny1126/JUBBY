# JUBBY Android Starter (v0.1)

This is a starter Android project for a Redmi 9A. It includes:
- A simple blue JUBBY interface
- Tap-to-speak using Android's speech-recognition activity
- Spoken responses using Android TextToSpeech
- Basic commands: greeting, time, date, open YouTube, open Settings, toggle flashlight

## Important limitations
- This is source code, not an APK.
- “Hey JUBBY” always-on wake-word detection is NOT implemented.
- Speech recognition may require internet and a speech recognition provider on the phone.
- It is not an unrestricted phone-control tool; Android permissions and app availability apply.
- The starter has not been tested on a physical Redmi 9A. Treat it as a prototype.
- Do not install APKs from unknown sources; build from this source and review permissions.

## Free build from a phone using GitHub Actions
1. Sign in to GitHub and create a new public or private repository named `JUBBY`.
2. On GitHub's website, upload the contents of this folder (not the enclosing folder) to the repository. Ensure `.github/workflows/build-apk.yml` is included; hidden files can be easy to miss on mobile.
3. Open the repository's **Actions** tab. If prompted, enable Actions.
4. Select **Build JUBBY APK** and tap **Run workflow**. Alternatively, pushing the files to `main` starts a build.
5. Wait for the workflow to finish successfully.
6. Open the completed workflow run and download the `JUBBY-debug-APK` artifact.
7. Extract the ZIP on your phone to get `app-debug.apk`, then tap it to install. Android may ask you to allow installation from that browser/file manager. Only proceed if you trust the source and you initiated the build.
8. Launch JUBBY and grant microphone permission. Tap **TAP TO SPEAK** and test “Hello JUBBY”, “What time is it?”, “Open YouTube”, “Open Settings”, and “Turn on flashlight”.

If upload of hidden `.github` files is difficult in mobile browser, use GitHub's mobile-friendly web UI or the repository upload flow that supports folders. The workflow must exist at `.github/workflows/build-apk.yml`.

## Technical stack
Java + Android SDK, minSdk 23, targetSdk 28, Gradle 8.9, Android Gradle Plugin 8.7.3. GitHub Actions provides the free build environment subject to GitHub account limits and current plan rules.
