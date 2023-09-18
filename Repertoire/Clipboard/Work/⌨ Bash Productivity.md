Most frequently used bash commands for office productivity or general daily driver usage.

## First-Party Repository
### Archive
**Extract \*.rar files**
`unrar x file-name.rar`

### Office
**PDF to Image**
`pdftoppm inputname.pdf outputname -png`

**PNG to TXT**
`tesseract -l eng inputname.png outputname  `

**FFMPEG Conversion**
`ffmpeg -i item1.extension1 item1.extension2`
### Location
**Root \*.desktop location**
`/usr/share/applications`

**Flatpak \*.desktop location**
`~/.local/share/applications`

## Python Pip Repository
**gallery-dl Frequent Commands**
Download from range of 1 to 100
`gallery-dl --range 1-100 URL`

Create archive of already downloaded images but do not download
`gallery-dl --download-archive ARCHIVE.txt --no-download -o skip=false  `

Create archive of images
`gallery-dl --download-archive ARCHIVE.txt`

gallery-dl Configuration Location
Windows: `%APPDATA%\gallery-dl\config.json`
Linux: `/etc/gallery-dl.conf`

gallery-dl Cookies
`gallery-dl --cookies-from-browser Firefox`

## Third-Party Repository
**NodeJS Version Manager**
```$ nvm use 16
Now using node v16.9.1 (npm v7.21.1)
$ node -v
v16.9.1
$ nvm use 14
Now using node v14.18.0 (npm v6.14.15)
$ node -v
v14.18.0
$ nvm install 12
Now using node v12.22.6 (npm v6.14.5)
$ node -v
v12.22.6`
```