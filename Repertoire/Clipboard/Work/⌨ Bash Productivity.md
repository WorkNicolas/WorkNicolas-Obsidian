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

## Linux Setup
### Font
```
sudo nano /etc/environment

FREETYPE_PROPERTIES="cff:no-stem-darkening=0 autofitter:no-stem-darkening=0"
```

### Fedora Post-Install
**DNF Configuration**
```
sudo nano /etc/dnf/dnf.conf

# Add the following
fastestmirror=True
max_parallel_downloads=10
defaultyes=True
keepcache=True

# Clean
sudo dnf clean all
```

**System Update**
```
sudo dnf update
```

**Enable RPM Fusion**
```
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm

sudo dnf groupupdate core
```

### Add Flatpak
```
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

### Change Hostname
```
sudo hostnamectl set-hostname fedora38
```

### Add Media Codecs
```
sudo dnf groupupdate multimedia --setop="install_weak_deps=False" --exclude=PackageKit-gstreamer-plugin
```

