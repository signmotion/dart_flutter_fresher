## Features

We can choose with **CrossFileManager** the priority for uploaders yourself. For example, if the file is not in the assets, an attempt will be made to get the file from the cloud.

Can develop own loader for download files from Firebase, Firestore, Amazon AWS, Google Drive, Microsoft Azure Cloud Storage, OneDrive, Dropbox, etc. - any data source can be included in the CrossFileManager. See `class Loader` and [already implemented loaders](https://github.com/signmotion/cross_file_manager/tree/master/lib/src/loaders).

Can retrieve the needed file from an archive. It comes in handy when you need to download thousands of small files.

Can memorize a received file and retrieve it from local storage the next time it is requested.

Able to download files in formats:

- `String`
- `Image` like `dart.ui`
- `Image` like `package:flutter/widgets.dart`
- `File`, binary data

### How it works

[<img src="https://raw.githubusercontent.com/signmotion/cross_file_manager/master/images/request_response.webp" width="600"/>](https://raw.githubusercontent.com/signmotion/cross_file_manager/master/images/request_response.webp)

## Usage

### Create a Manager for App

```dart
final fm = CrossFileManager.create(
  loaders: const [
    PlainAssetsLoader(),
    ZipAssetsLoader(),
    PlainFileLoader(),
    ZipFileLoader(),
  ],
);
```

### Use the Manager in App

```dart
final r = await fm.loadString(path);
```

```dart
final r = await fm.loadFile(path);
```

```dart
final r = await fm.loadImageUi(path);
```

```dart
final r = await fm.loadImageWidget(path);
```

```dart
final r = await fm.exists(path);
```

```dart
final r = await fm.existsInCache(path);
```

```dart
// Just add a file to cache for fast access in the future.
await fm.warmUp(path);
```

The manager announced above will search file by `path` in the local assets,
then in the zip archives of local assets,
then in the local filesystem,
then in the zip archives of local filesystem.

It will return the first file found.

See `example/main.dart` for more use cases:

[<img src="https://raw.githubusercontent.com/signmotion/cross_file_manager/master/images/screenshots/zip_assets_demo.webp" width="600"/>](https://github.com/signmotion/cross_file_manager/tree/master/example)
