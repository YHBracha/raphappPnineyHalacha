# Development Guide

This document outlines the setup and development process for the **raphappPnineyHalacha** Android project.

## Project Setup

### Required Tools
- **JDK Version:** 17
- **Gradle Version:** 9.5.1
- **Android Gradle Plugin (AGP) Version:** 9.2.1
- **Android Studio:** Latest stable version recommended.

### SDK Configuration
These values are defined in `app/build.gradle`:
- **compileSdk:** 37
- **minSdk:** 23
- **targetSdk:** 34

## Getting Started

### How to open the project in Android Studio
1. Launch Android Studio.
2. Select **File > Open**.
3. Navigate to the root directory of this project (`raphappPnineyHalacha`).
4. Click **OK**.
5. Wait for the Gradle sync to complete.

### How to build a debug APK
You can build the debug APK using either the IDE or the command line:

**Using Android Studio:**
1. Go to **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
2. Once finished, a notification will appear with a link to the `app-debug.apk` file.

**Using Terminal:**
```bash
./gradlew assembleDebug
```
The APK will be located at `app/build/outputs/apk/debug/app-debug.apk`.

### How to run the app on a connected device
1. Connect your Android device via USB and ensure **USB Debugging** is enabled in Developer Options.
2. In Android Studio, select your device from the target device drop-down menu in the toolbar.
3. Click the green **Run** button (or press `Shift + F10`).

Alternatively, via Terminal:
```bash
./gradlew installDebug
```

## Project Structure

### Main Folders
- `app/src/main/java`: Contains the Java source code for the application.
- `app/src/main/res`: Contains the application resources (layouts, drawables, strings, etc.).
- `app/src/main/assets`: Contains static content files, such as HTML books used within the app.
- `gradle/`: Contains the Gradle wrapper and version catalog (`libs.versions.toml`).

### Important Files
- `build.gradle`: Root-level build configuration.
- `app/build.gradle`: App-level build configuration.
- `settings.gradle`: Project settings and module inclusion.
- `gradle/libs.versions.toml`: Centralized dependency and version management.
- `app/src/main/AndroidManifest.xml`: Essential information about the app for the Android system.
