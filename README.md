# WMI Fix for Touhou: Shining Shooting Star

This is a minor patch fix for Touhou: Shining Shooting Star that allows it to be played under wine on linux.

**This patch fixes the following error: System.Management.ManagementException: Error code: 0x80041002**

## Changes/Fixes

1. Added overload for Dpi.GetDpi() Function to accept custom Dpi value.
2. Added new configuration entries under Mode (DPIX, DPIY)
3. Added a new windowSize value (3 = 1920x1080) (Not confirmed to work. Can be changed in the config.)

## Installation

1. Download the zip file in `Releases`
2. Extract the .exe file in your in your touhou installation folder.
3. Open the `Setting.INI` file and add the following entries Under `Mode`
```ini
DpiX={Your screen's Dpi X value}
DpiY={Your screen's Dpi Y value}
```
## Getting your screen's DPI values

The easiest way to get the DPI values is to use the command `xdpyinfo`
or you can calculate it manually. You can learn how to do that [here](https://winaero.com/blog/find-change-screen-dpi-linux/).

1. Open your terminal
2. Type `xdpyinfo | grep -B 2 resolution`
3. The resolution is your screen DPI (DpiX x DpiY dots per inch)

## WARNING

This patch was only tested in vanilla wine (64 bit), this might not work on other custom wine builds like lutris or proton.
