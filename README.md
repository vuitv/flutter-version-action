# Read Flutter SDK Version

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

This GitHub Action reads the Flutter SDK version from a `pubspec.yaml` file using `yq` and sets it as an output variable.

## Features

✅ Outputs flutter sdk version

> [!IMPORTANT]
>
> You need to have the exact Flutter version
> defined in your pubspec.yaml:
>
> **Good**
>
> ```yaml
> environment:
>   sdk: ">=3.3.0 <4.0.0"
>   flutter: 3.19.0
> ```
>
> **Bad**
>
> ```yaml
> environment:
>   sdk: ">=3.3.0 <4.0.0"
>   flutter: ">= 3.19.0 <4.0.0"
> ```

## Usage

Standard usage:

```yaml
steps:
  - name: 📍 Read Flutter SDK Version
    uses: vuitv/flutter-version-action@v3
    id: flutter-version-action

  - name: Use the Flutter version variable
    run: echo "The Flutter version is ${{ steps.flutter-version-action.outputs.version }}"
```

## Inputs

The action takes the following inputs:

- `pubspec-path`: The path to the `pubspec.yaml` file (default: `pubspec.yaml`).

## Outputs

The actions outputs the following:

- `version`: The Flutter SDK version.