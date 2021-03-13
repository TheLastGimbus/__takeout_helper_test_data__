# JSON Asserts

This folder contains some json files with list of asserts to be done on output files

These are just the correct values - the Python tests in [original repo](https://github.com/TheLastGimbus/GooglePhotosTakeoutHelper/)
should test if these are the same

Generally, all of them have this structure:
```json
{
  "photos": {  // Map of photos to test in output folder
    "received_1475305699271723.jpeg": {  // Key is the name of the file
      "someData": "dupa12" // some data to test
    },
    // Some asserts test just one value, so they don't have whole map:
    "received_2406590499662709.jpeg": 213769420
  },
  "videos": {
    "received_519991975518300.mp4": 54325342534
  }
}
```

### `file_modified.json`
Output file correct "last modified value"

```json
{
  "photos": {
    "photo1.jpg": 1556568359,  // Unix time
    "photo2.png": 1564350491
  },
  "videos": {
    "video1.mp4": 45353453,
  }
}
```

### `file_hash.json`
SHA1 hash of output photos

Because of exif values that change inside the file, you need to collect it *after* files came through the script
```json
"video12.webp": "fjdsfoweirndfsjgdfhngsda"  // The SHA1 hash
```

### `exif_dates.json`
Correct "photo taken" datetimes in exif - just a single unix integer

### `exif_location.json`
Correct gps coordinates that should be present in exif
```json
{
  "photos": {
    "received_1475305699271723.jpeg": {
      "lat": 49.210771,
      "lng": 22.6266861
    }
  }
}
```
