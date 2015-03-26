# synology-video-indexer

Problem: Files copied to a Synology NAS via RSYNC or SSH are not automatically indexed and the command `synoindex -R video` reindex everything.

This script reindex `/volume1/video/` adding or removing only what is needed, comparing the mediaserver database and file system contents based on file paths, file size and mtime are not considered.

## Usage

```
indexvideo [-n]

	-n    dry run
```

## Note

If you have a php warning `open_basedir restriction in effect` add needed paths to `open_basedir` in `/etc/php/conf.d/user-settings.ini` or `/etc.defaults/php/conf.d/user-settings.ini`

//