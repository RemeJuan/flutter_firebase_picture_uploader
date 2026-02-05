# Copilot Instructions for Firebase Picture Uploader

## Project Overview
This is a Flutter package that provides a widget for uploading pictures to Firebase Storage. The library is published on pub.dev and focuses on providing a simple, customizable image upload widget with Firebase integration.

## Tech Stack
- **Language**: Dart (SDK >= 3.0.6)
- **Framework**: Flutter (>= 3.22.0)
- **Backend**: Firebase (Storage, Core)
- **Key Dependencies**:
  - `firebase_storage`: ^12.1.3
  - `firebase_core`: ^3.3.0
  - `image_picker`: ^1.1.2
  - `image_cropper`: ^8.0.1
  - `cached_network_image`: ^3.2.3

## Build and Test Commands
- `flutter pub get` — Install dependencies
- `flutter analyze` — Run static analysis with configured linter rules
- `flutter test` — Run tests (if available)
- `cd example && flutter run` — Run the example app
- `flutter pub publish --dry-run` — Validate package before publishing

## Code Style and Conventions

### General Guidelines
- Follow the linter rules defined in `analysis_options.yaml`
- Use single quotes for strings (as per `prefer_single_quotes` rule)
- Always declare return types explicitly
- Prefer const constructors where possible
- Use camel case for types and identifiers
- Annotate overrides explicitly

### Dart-Specific Conventions
- Always use explicit return types for functions and methods
- Prefer final fields and locals where applicable
- Use collection literals instead of constructors
- Avoid bool literals in conditional expressions
- Place control flow body on new line
- Use proper null safety patterns

### Flutter-Specific Conventions
- Follow Flutter widget composition patterns
- Use StatefulWidget for widgets with mutable state
- Use StatelessWidget for widgets with immutable state
- Prefer const constructors for performance
- Use proper lifecycle methods (initState, dispose, etc.)

## Project Structure
```
lib/
  firebase_picture_uploader.dart    # Main library export file
  src/
    firebase_picture_upload_controller.dart  # Controller logic
    firebase_picture_uploader_widget.dart   # Main widget
    firestore_image.dart                    # Image handling
example/
  lib/main.dart                     # Example usage
```

## Firebase Integration
- This package requires Firebase to be configured in the host application
- Users must add their own GoogleService-Info.plist (iOS) or google-services.json (Android)
- The package uses Firebase Storage for image uploads
- Always handle Firebase exceptions gracefully

## Widget Behavior
- The `PictureUploadWidget` supports single and multiple image uploads
- Provides image selection, cropping, and deletion functionality
- Highly customizable (fonts, colors, text, etc.)
- Uses image_picker for platform-specific image selection
- Uses cached_network_image for efficient image loading

## Important Notes
- This is a library package, not an application
- Changes should maintain backward compatibility when possible
- The package is published on pub.dev, so API changes need versioning consideration
- Always test with the example app before submitting changes
- Maintain compatibility with the specified SDK versions

## Commit Message Convention
- Use descriptive commit messages
- Reference issue numbers when applicable
- Keep commits focused and atomic

## Pull Request Guidelines
- Test changes with the example app
- Run `flutter analyze` to ensure no linting errors
- Update CHANGELOG.md for notable changes
- Update version in pubspec.yaml if needed (following semantic versioning)
- Update documentation if API changes are made
