# Fakhri Quran Studio — Klencod IDE / Android APK

## Project type
This is a native Android project written in Kotlin + Jetpack Compose (not a web-only project). Open/import the **extracted project root** — the folder containing `settings.gradle.kts`, `build.gradle.kts`, and `app/`.

## Import and build in Klencod IDE
1. Extract this ZIP completely.
2. In Klencod IDE, choose Open/Import existing Android/Gradle project and select the extracted root folder.
3. Allow Gradle sync and Android SDK downloads to finish. Use JDK 17 or the JDK recommended by the IDE for its installed Android Gradle Plugin.
4. If the IDE reports that Gradle wrapper files are missing, choose the IDE's installed Gradle distribution / generate a Gradle wrapper from the IDE. This ZIP does not include `gradlew`, `gradlew.bat`, or `gradle-wrapper.jar`.
5. Select the `app` run configuration/module and build the debug APK.
6. Typical output path: `app/build/outputs/apk/debug/app-debug.apk`.

## Important configuration notes
- `google-services.json` is not included. The build config is set to warn if Firebase configuration is missing, but Firebase-backed features may need project configuration/API credentials before they can run.
- `.env.example` is a template only. Do not put private API keys in a public ZIP or commit them to source control.
- Building an APK requires an Android SDK and a compatible JDK/Gradle environment. This archive has not been compiled in this environment, so a successful APK build cannot be guaranteed until Gradle sync/build completes in Klencod.

## If build fails
Copy the **first actual Gradle/Kotlin error** from the Build output and give it to Klencod's coding assistant with the prompt in `KLENCOD_BUILD_PROMPT_AR.txt`. Fix the underlying error and rebuild; do not merely suppress errors or replace working app features with placeholders.
