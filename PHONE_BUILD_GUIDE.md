# SNAPFIX Cloud Build v0.2.1

This package is prepared for a phone-only cloud build.

## What this build produces
- Android debug APK
- No Android Studio required on your phone
- Cloud build configuration included
- Existing SNAPFIX local/offline MVP features preserved

## Phone-only steps

1. Create/sign in to a GitHub account in your phone browser/app.
2. Create a new repository, for example: `snapfix-app`.
3. Upload ALL files from this ZIP into the repository.
4. Open Codemagic and connect that GitHub repository.
5. Select the `codemagic.yaml` workflow named `SNAPFIX Android APK`.
6. Start the build.
7. When the build finishes, download the APK from Codemagic Artifacts.

The workflow installs Gradle 8.9 in the cloud if Gradle is not already available, then runs `assembleDebug`.

Note:
- This is a debug APK for testing, not yet a Play Store release AAB.
- Google Play release signing will be added after the APK works on the phone.
- Real AI APIs, AdMob, subscriptions, and backend are not included in this build yet.
