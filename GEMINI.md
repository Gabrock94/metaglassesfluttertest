# Meta Wearables DAT Flutter Project

This project is a Flutter implementation utilizing the Meta Wearables DAT SDK.

## Package Information
- **Package**: [flutter_meta_wearables_dat](https://pub.dev/packages/flutter_meta_wearables_dat)

## API Reference Summary (v0.17)

The SDK provides a cross-platform framework for Meta AI glasses.

### Core Components
- **MWDATCore**: Registration, device discovery, and session management.
- **MWDATCamera**: Camera access, streaming (720p), and photo capture.
- **MWDATDisplay**: Declarative UI toolkit for glasses display.

### Key Classes & Methods
| Class | Key Methods / Properties |
| :--- | :--- |
| **Wearables** | `configure()`, `startRegistration()`, `devicesStream` |
| **DeviceSession** | `start()`, `stop()`, `addStream()`, `addDisplay()` |
| **Stream** | `start()`, `videoFramePublisher`, `capturePhoto()` |
| **Display** | `send(view)`, `statePublisher` |

### Flutter Mapping Patterns
- **Lifecycle**: Map `SessionState` to Flutter app states.
- **Streams**: Use `EventChannel` for `devicesStream` and `videoFramePublisher`.
- **UI**: Flutter widgets mirrored as DAT `FlexBox` trees.

## Project Structure
- `lib/main.dart`: Entry point of the example app.
- `lib/flutter_meta_wearables_dat.dart`: Core plugin interface.
- `lib/meta_wearables_dat_method_channel.dart`: Method channel implementation.
- `lib/meta_wearables_dat_platform_interface.dart`: Platform interface.

## Setup Requirements
- **Secrets**: Meta App ID and Client Token required.
  - iOS: `ios/Flutter/Secrets.xcconfig`
  - Android: `android/secrets.properties`
