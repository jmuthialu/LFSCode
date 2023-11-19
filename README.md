# Source controlling large files greater than 100MB

## Install lfs client
$ brew install git-lfs

## Configuring LFS

$ git lfs track "heresdk-navigate-android-4.16.2.0.12878.aar"
This will create `.gitattributes` file which contains

`heresdk-navigate-android-4.16.2.0.12878.aar filter=lfs diff=lfs merge=lfs -text` 

<br>
$ git add -A

$ git commit -m "Adding lfs tracker"

Now add the large file to repo and the add to git.


$ cp ~/.heresdk-navigate-android-4.16.2.0.12878.aar .

$ git add heresdk-navigate-android-4.16.2.0.12878.aar

$ git commit -m "adding sdk"

$ git push
```
Uploading LFS objects: 100% (1/1), 117 MB | 9.8 MB/s, done.
```