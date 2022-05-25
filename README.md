# DarkSwitcher
This is a free application for Windows 10, what helps you to schedule switching between dark and light theme automatically.

I can't provide the source code right now, you can download the installer only. Publishing source code is in my future plans.

## Download and install

### Using installer exe
You can download the installer of the latest version by clicking on the [Releases](https://github.com/iminet/darkswitcher/releases) link. By choosing the latest version, click on the `DarkSwitcherSetupx.x.xxxx.exe` to download the installer. After the installer downloaded, you can run the installer like any Windows programs.

### Using winget
With winget, it is very easy to install the latest release

`winget install Iminetsoft.Darkswitcher`

## System requirements
- a PC running Windows 10 (x86 or x64)
- [.NET Framework 4.8 or newer](https://dotnet.microsoft.com/download/dotnet-framework)
- a few megabytes of free space on your SSD/HDD

## Screenshots
Here's the main window of the application in light...

![Main window](https://i.ibb.co/RN39Brx/darkswitcher-screenshot-1-0-7780.png)

... and in dark

![Main window](https://i.ibb.co/8df6c1f/darkswitcher-screenshot-dark-1-0-7780.png)

## Important
This tool works on Windows 10 only. If you install this tool on other operating systems, switching between dark/light theme won't work.

## Command line (CLI)
This software has limited, experimental CLI functionality. There's no visual feedback in CLI mode. After using a command, the application will return and throws `0` exit code (what means: terminated without any failure).

### Usage
```
darkswitcher [OPTIONS]
```

### Options
Options are case-sensitive. There are two ways to use multiple options in the same time:
- separated mode: each multi-character option is followed after double dash (--): `--console --toggle`
- merged mode: all single-character options are followed after a simple dash (--): `-cT`. All options should be a single character
```
-c, --console						Launch in CLI mode
-T, --toggle						Toggle between light and dark mode
-D, --dark							Switch to dark mode
-L, --light							Switch to light mode
```

### Launch in CLI mode
To start your application in CLI mode, showing without the main form, use the following option
```
darkswitcher --console
# OR
darkswitcher -c
```

### Examples
Never forget to use `--console` (separated) or `-c` (merged) option, elseway you'll get the main window instead your desired CLI command.
The options are case sensitive! Don't be confused, `-c` isn't equal to `-C`
```
# Switch between dark and light mode:
darkswitcher --console --toggle
# or
darkswitcher -cT

# Switch to light (no effect if you're already in light mode):
darkswitcher --console --light
# or
darkswitcher -cL

# Switch to dark (no effect if you're already in dark mode):
darkswitcher --console --dark
# or
darkswitcher -cD
```

## Feedback
Since this software is under development, your feedbacks are highly welcomed. Thank you! If you're getting bugs or unwanted behaviors, please report it me first, instead of negative or swearing comments.
