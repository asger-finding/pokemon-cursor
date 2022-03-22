# pokemon-cursor

An unofficial opensource Pokemon cursor theme for Windows and Linux.

[![build](https://github.com/ful1e5/pokemon-cursor/actions/workflows/build.yml/badge.svg)](https://github.com/ful1e5/pokemon-cursor/actions/workflows/build.yml)
[![CodeFactor](https://www.codefactor.io/repository/github/ful1e5/pokemon-cursor/badge)](https://www.codefactor.io/repository/github/ful1e5/pokemon-cursor)
[![Twitter](https://img.shields.io/badge/twitter-ful1e5-blue)](https://twitter.com/ful1e5)

#### Cursor Sizes

<kbd>22</kbd>
<kbd>24</kbd>
<kbd>28</kbd>
<kbd>32</kbd>
<kbd>40</kbd>
<kbd>48</kbd>
<kbd>56</kbd>
<kbd>64</kbd>
<kbd>72</kbd>
<kbd>80</kbd>
<kbd>88</kbd>
<kbd>96</kbd>

#### Colors

![#FFCB05](https://imgur.com/Q3Y7xFo.png)
![#3C5AA6](https://imgur.com/rlKmamu.png)
![#0070B6](https://imgur.com/epcnFzB.png)
![#000000](https://imgur.com/ScBWhdE.png)
![#ffffff](https://imgur.com/AiR8P8t.png)

### Quick install

- [https://www.pling.com/p/1701595](https://www.pling.com/p/1701595)

#### Preview:

> Check [Figma](https://www.figma.com/file/OoAFKT3u1HkzSe74QrLarQ/pokemon-cursor?node-id=0%3A1) file for .svg files.

<p align="center">
  <img title="Pokemon" src="https://imgur.com/Xhm2xgS.png">
  </img>
  <sub>Pokemon Cursors</sub>
</p>

### Manual Install

> Note: replace name according package name.

#### Linux/X11

```bash
# extract `Pokemon.tar.gz`
tar -xvf Pokemon.tar.gz

# For local users
mv Pokemon ~/.icons/

# For all users
sudo mv Pokemon /usr/share/icons/
```

#### Windows

1. unzip `Pokemon-Windows.zip` file
2. Open `Pokemon-Windows/` in Explorer, and **right click** on `install.inf`.
3. Click 'Install' from the context menu, and authorize the modifications to your system.
4. Open _Control Panel > Personalization and Appearance > Change mouse pointers_, and select **Pokemon Cursors**.
5. Click '**Apply**'.

### Uninstall

#### Linux/X11

```bash
# From local users
rm -rf ~/.icons/Pokemon

# From all users
sudo rm -rf /usr/share/icons/Pokemon
```

#### Windows

1. Go to **Registry Editor** by typing the same in the _start search box_.
2. Expand `HKEY_CURRENT_USER` folder and expand `Control Panel` folder.
3. Go to `Cursors` folder and click on `Schemes` folder - all the available custom cursors that are installed will be listed here.
4. **Right Click** on the name of cursor file you want to uninstall; for eg.: _Pokemon Cursors_ and click `Delete`.
5. Click '**yes**' when prompted.

# Dependencies

## External Libraries

- libxcursor
- libx11
- libpng (<=1.6)

#### Install External Libraries

##### macOS

```bash
brew install --cask xquartz
brew install libpng
```

##### Debain/ubuntu

```bash
sudo apt install libx11-dev libxcursor-dev libpng-dev
```

##### ArchLinux/Manjaro

```bash
sudo pacman -S libx11 libxcursor libpng
```

##### Fedora/Fedora Silverblue/CentOS/RHEL

```bash
sudo dnf install libX11-devel libXcursor-devel libpng-devel
```

## Build Dependencies

- [gcc](https://gcc.gnu.org/install/)
- [make](https://www.gnu.org/software/make/)
- [nodejs](https://nodejs.org/en/) (<=12.x.x)
- [yarn](https://classic.yarnpkg.com/en/docs/install/)
- [python](https://www.python.org/downloads/) (<=3.8)
- [pip3](https://pip.pypa.io/en/stable/installing/)

### Node Packages

- [puppeteer](https://www.npmjs.com/package/puppeteer)
- [pngjs](https://www.npmjs.com/package/pngjs)
- [pixelmatch](https://www.npmjs.com/package/pixelmatch)

### PyPi Packages

- [clickgen](https://pypi.org/project/clickgen/s)

## Build From Scratch

### Auto Build (using GitHub Actions)

GitHub Actions is automatically runs on every `push`(on **main** and **dev** branches) and `pull request`(on **main** branch), You found theme resources in `artifact` section of **build**.GitHub **Actions** source is available inside [.github/workflows](https://github.com/ful1e5/pokemon-cursor/tree/main/.github/workflows) directory.

### Manual Build

> Check **[Makefile](./Makefile)** for more targets.

```bash
make
```

#### Build `XCursor` theme

```bash
make unix
```

#### Customize `XCursor` size

```bash
make unix X_SIZES=22            # Only built '22px' pixel-size.
make unix X_SIZES=22 24 32      # Multiple sizes are provided with  ' '(Space)
```

#### Install `XCursor` theme

```bash
make install            # install as user
  # OR
sudo make install       # install as root
```

#### Build `Windows` theme

```bash
make windows
```

#### Customize `Windows Cursor` size

```bash
make windows WIN_SIZE=96            # Supports only one pixel-size
```

> For installation follow [these](#windows) steps.

# Bugs

Bugs should be reported [here](https://github.com/ful1e5/pokemon-cursor/issues) on the Github issues page.

# Getting Help

You can create a **issue**, I will help you. 🙂

# Contributing

Check [CONTRIBUTING.md](CONTRIBUTING.md), any suggestions for features and contributions to the continuing code masterelopment can be made via the issue tracker or code contributions via a `Fork` & `Pull requests`.
