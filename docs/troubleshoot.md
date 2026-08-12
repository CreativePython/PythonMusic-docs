---
hide_localnav: true
---

# Troubleshooting Pip

## Missing C/C++ Build Tools

Most ```pip install``` problems come from the same cause.  A few of PythonMusic's dependencies are written partly in C or C++.  When a ready-made version isn't available for your computer, ```pip``` builds that dependency from its source code instead — and building needs tools that don't come with Python.

This is your problem if the installation stops with a message like:

- ```CMake configuration failed```
- ```Failed building wheel for python-rtmidi```
- ```Failed building wheel for pyaudio```
- ```error: command 'clang' failed```
- ```error: Microsoft Visual C++ 14.0 or greater is required```

The simplest fix is to install Python 3.12, instead of 3.13 or later.  On Python 3.12, all of PythonMusic's dependencies offer ready-made versions, so ```pip``` won't need to build anything.

If you want to use Python 3.13 or later, or you're already using 3.12 and still seeing one of these messages, the fix is to install the missing tools, then run ```pip install PythonMusic``` again.

### Step 1: Install the C/C++ build tools

This is what ```pip``` needs in order to build anything at all, and it resolves most of the errors above.

- **On Windows**, download and install [Visual Studio Build Tools 2022](https://visualstudio.microsoft.com/downloads/).  In the Visual Studio installer, make sure "Desktop development with C++" is checked.  Restart your computer, then try installing PythonMusic again.

- **On macOS**, open Terminal and type:

    ```
    xcode-select --install
    ```

    A dialog will appear — click "Install" to install Apple's Command Line Tools and wait for it to finish.  Then, try installing PythonMusic again.

### Step 2 (macOS only): Install PortAudio

If the installation still stops with ```Failed building wheel for pyaudio```, or mentions ```fatal error: 'portaudio.h' file not found```, you also need PortAudio — a sound library that PythonMusic uses to play audio.

The easiest way to get it is with [Homebrew](https://brew.sh), a package manager for macOS.  If you don't already have Homebrew, run the one-line install command on [brew.sh](https://brew.sh).  Then, in Terminal, type:

```
brew install portaudio
```

Then try installing PythonMusic again.

---

## Rosetta / x86_64 Build Issues

If you set up your Apple Silicon Mac by migrating from an older Intel Mac, some programs may have carried over in their Intel form and now run through Rosetta, Apple's translation layer for Intel software.  When that happens, ```pip``` builds Intel (```x86_64```) versions of PythonMusic's dependencies, which then won't load on your processor.

This is your problem if the installation stops with a message like:

```
mach-o file, but is an incompatible architecture (have 'x86_64', need 'arm64')
```

### Step 1: Make sure Terminal isn't running under Rosetta

1. In Finder, go to your System Applications (not your User Applications).

    - Select "Go" in the Menu Bar, select "Go To Folder", and enter `/Applications/`

2. Open "Utilities"

3. Hold the "Control" key and click "Terminal", and select "Get Info"

4. Make sure "Open using Rosetta" is not checked.

### Step 2: Rebuild for Apple Silicon

#### Python

First, check which architecture your Python is running as:

```
python3 -c "import platform; print(platform.machine())"
```

This should print ```arm64```.  If it prints ```x86_64```, your Python is running under Rosetta and needs to be reinstalled.  Installing from an [official Python Installer](https://www.python.org/downloads/) will give you a version that runs natively on Apple Silicon.

#### PythonMusic Dependencies

```tinysoundfont``` is the most common offender — to force tinysoundfont to build for Apple Silicon, enter this command:

**NOTE:** This builds from source, so you'll need the [C/C++ build tools](#missing-cc-build-tools) first.

```
env ARCHFLAGS="-arch arm64" pip install --force-reinstall --no-cache-dir --no-binary tinysoundfont tinysoundfont
```

Other dependencies can be reinstalled similarly, using the same command but replacing both instances of ```tinysoundfont``` with the name of the dependency.

---

## Still Stuck?

Let us know on [GitHub](https://github.com/CreativePython/PythonMusic/issues).