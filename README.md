<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# LeviLab Launcher

View your app in AI Studio: https://ai.studio/apps/01c790b4-239e-45af-b85c-8ba1129897c8

## Build locally

Install Android Studio with the Android SDK for API 36.1. Use JDK 21 for the
build and test commands below, since running Robolectric tests on Android API
36 requires it. The debug APK alone can also be built with JDK 17.
Extract the archive and open the folder containing `settings.gradle.kts`.
You can also build a debug APK and run unit tests from that folder:

```sh
./gradlew :app:assembleDebug :app:testDebugUnitTest
```

On Windows, use `gradlew.bat` instead of `./gradlew`. If you build outside
Android Studio, set `ANDROID_HOME` to your SDK installation path. The debug
APK is written to `app/build/outputs/apk/debug/app-debug.apk`.

No Gemini API key is needed for the current launcher features. A local debug
build uses Android's default debug signing unless you provide the original
`debug.keystore` in the project root. A build signed with a different key cannot
update an existing installation with the same app ID.

Release signing is separate and still uses the original upload key configuration.
