# Source controlling large files greater than 100MB

## Install lfs client
$ brew install git-lfs

## Configuring LFS (for Androd aar)

Initialize lfs for this repo. This is one time activity per repo.

$ git lfs install

$ git lfs track "heresdk-navigate-android-4.16.2.0.12878.aar"
This will create `.gitattributes` file which contains

`heresdk-navigate-android-4.16.2.0.12878.aar filter=lfs diff=lfs merge=lfs -text` 

<br>
$ git add -A

$ git commit -m "Adding lfs tracker"

$ git push

Now add the large file to repo and the add to git.


$ cp ~/.heresdk-navigate-android-4.16.2.0.12878.aar .

$ git add heresdk-navigate-android-4.16.2.0.12878.aar

$ git commit -m "adding sdk"

$ git push
```
Uploading LFS objects: 100% (1/1), 117 MB | 9.8 MB/s, done.
```


## Configuring LFS (for iOS xcframework)

$ git lfs track "heresdk.xcframework/**"

"**" will recusrively add contents under xcframework folder and will modify  `.gitattributes` file which now contains

```
heresdk-navigate-android-4.16.2.0.12878.aar filter=lfs diff=lfs merge=lfs -text
heresdk.xcframework/** filter=lfs diff=lfs merge=lfs -text

```

$ git add -A

$ git commit -m "Adding lfs tracker for ios"

$ git push

Now add the large file to repo and the add to git.


$ cp ~/heresdk.xcframework .

$ git add -A

$ git commit -m "adding sdk"

$ git push
```
Uploading LFS objects: 100% (1/1), 117 MB | 9.8 MB/s, done.
```
