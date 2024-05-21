# Read Flutter SDK Version

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

This GitHub Action reads the Flutter SDK version from a `pubspec.yaml` file using `yq` and sets it as an output variable.

## Features

✅ Outputs flutter sdk version

## Usage

Standard usage:

```yaml
steps:
  - name: 📍 Read Flutter SDK Version
  - uses: vuitv/flutter-version-action@v1

  - name: Use the Flutter version variable
    run: echo "The Flutter version is ${{ steps.flutter-version-action.outputs.flutter-version }}"
```

## Inputs

The action takes the following inputs:

- `pubspec-path`: The path to the `pubspec.yaml` file (default: `pubspec.yaml`).

## Outputs

The actions outputs the following:

- `flutter-version`: The Flutter SDK version.