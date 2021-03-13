# __takeout_helper_test_data__

## What is this?
This is the repo that contains images for testing [GooglePhotosTakeoutHelper script](https://github.com/TheLastGimbus/GooglePhotosTakeoutHelper/)

## The rules
ALL photos and videos MUST have all of their expected properties fully tested. That is, if you upload a .jpg here that
is expected to contain some location data (either from json or itself), you *have* to add both location test in
[asserts/exif_location.json](asserts/exif_location.json), as well as [file modified](asserts/file_modified.json),
[exif date](asserts/exif_dates.json) and [file hash](asserts/file_hash.json).

## Versioning
We version everything with a tag here. Then, in the original repo, if you want to update to new set of photos
to test on, you need to checkout on new version

## TODO:
I'm not certain if checking file hashes is fully good idea - if we change the way we write exifs in *any way*,
almost all of them will fail (I think) - so I may remove them in future
