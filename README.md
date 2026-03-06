# Smart Solar Panel Orientation System (SSOPS)

Android app + Arduino firmware for solar panel tracking, orientation, and monitoring.

## Project structure

- `app/`: Android application (Kotlin)
- `Arduino Code/`: Arduino sketches (tracking + WiFi controller)

## Requirements

- Android Studio (recommended latest stable)
- Android SDK `compileSdk 34`, `minSdk 24`
- JDK (as required by Android Studio/Gradle)

## Run (Android app)

1. Open the `SSOPS` project folder in Android Studio.
2. Sync Gradle.
3. Run the app on an emulator or a physical device.

### CLI (optional)

```bash
./gradlew :app:assembleDebug
```

## Network / Device API

The app uses an HTTP API (Retrofit). Make sure the device IP/base URL is set (default `192.168.1.4`).

### Endpoints

- `GET /status`
- `GET /consumption?days=N`
- `POST /control`

### Sample payloads

- Enable auto tracking:

```json
{ "autoTracking": true }
```

- Set manual angle:

```json
{ "angle": 10 }
```


