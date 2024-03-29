Tekken Overlay
==============

This software is intended for educational purposes only. The software is not to
be used to gain competetive advantage. We take no responsibility for misuse of
this software in a competitive setting.

How to use
-------

Download and install VC++ 2015-2019 Redistributables(vc_redist.x64.exe file) from [here](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads).  
Download Tekken Overlay.  
[here​​​](https://github.com/TekkenOverlay/TekkenOverlay/releases/latest): Download the top `.zip` file.  
Extract zip to anywhere: you need to actually extract the `.zip` archive and __not__ just double click it to open it in the explorer.  
Run TekkenOverlay.exe.  
Run Tekken.  
Once you get to main menu, press F1 to open the main menu.

Problems
--------

### Searching for process ID... NOT FOUND

#### Fix #1 

If Steam or Tekken with Administrator privileges, you need to also run the `tekken-overlay-run.exe` as Administrator.

If this doesn't work, go over the `Injecting DLL... FAIL!` fixes below.

### Injecting DLL... FAIL!

#### Fix #1

This might mean you haven’t extracted `.zip` archive and running your `tekken-overlay-run.exe` file
from inside the `.zip` archive. Extract your `.zip` archive as instructed in the
[Install section](https://github.com/TekkenOverlay/TekkenOverlay#install) and
then run the `tekken-overlay-run.exe` file.

#### Fix #2

Another reason you can get this error is because VC++ Redistributables installed on your machine.

Install VC++ Redistributables 2015-2022 from [here](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads): x86 and x64 downloads.

#### Fix #3

Use a different injector and inject the `tekken-overlay.dll` file into the `TekkenGame-Win64-Shipping.exe` process using that third-party injector, such as [Extreme Injector](https://github.com/master131/ExtremeInjector/releases/latest). [Demonstration video on how to do it](https://user-images.githubusercontent.com/16989713/149813511-1225eb7c-7ad5-49cf-a9b9-34193e601cc1.mp4). Any other injector capable of working with 64-bit executables should work, too.

#### Fix #4

If neither of the injectors worked and you still can't inject with neither `tekken-overlay-run.exe`, nor a third-party injector, it could be an issue with dependencies on your machine.

Try injecting a [Hello World dll](https://github.com/carterjones/hello-world-dll) using a third-party injector to test that injection works on your machine in general. [Video Demonstration](https://user-images.githubusercontent.com/16989713/149820814-21394c83-0efa-4e68-a79e-388c6d049e51.mp4).

If you get an error injecting the Hello World dll or if you don't see the Hello World message box after injection, then you have some problem on your machine and the default injection method doesn't work in general on your machine(and it should work). A possible fix is to install [Windows SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/) and [Windows DDK](https://docs.microsoft.com/en-US/windows-hardware/drivers/download-the-wdk#download-icon-step-3-install-windows-11-wdk). Both of these work on Windows 7 - 11 and will install missing dependencies, absence of which could cause the issue.

#### Fix #5

Another way to make the overlay work is to use a different injection method: make the overlay a dependency of the game and let the game load the overlay itself each game start. Follow [the wiki article](https://github.com/TekkenOverlay/TekkenOverlay/wiki/Making-the-game-automatically-load-the-overlay-on-the-game-start) on how to do it.

### Not working framedata overlay

If framedata and/or hitboxes don't show up but game information and throw counter work, check that your rendering scale is set to 100.
Tekken 7 Main menu → Settings → Graphics Settings → Rendering Scale → Set to 100

### Windows Defender or any other antivirus deletes downloaded files

Your antivirus software mistakenly thinks it's a virus because they don't really know if something is a virus or not. They just look at sets of functions the program uses and **assume** if something is a virus or not. You can read about false positives [here](https://www.tomsguide.com/news/what-are-false-positives-and-how-to-avoid-them) or just [google](https://www.google.com/search?q=Antivirus+false+positives) it yourself.

#### Ways to make the overlay work if antivirus deletes files or blocks it from running

1. One way to stop the antivirus software complaining about it is to add the zip file and/or extracted files to the exceptions of your antivirus.
2. Another way is to download an older version of the overlay and copy that old `tekken-overlay-run.exe`(when your antivirus didn't complain) to the folder where you extracted the new version, and just run it. This file does not change from version to version and works on all overlay and Tekken versions.
3. Third option is not to use our `tekken-overlay-run.exe` injector, but to use a third-party injector. Any injector that's capable to work with 64-bit executables on Windows will do.
Just inject the `tekken-overlay.dll` file into `TekkenGame-Win64-Shipping.exe` running process(you need a running game to inject into).

Some people get concerned that the Overlay gets flagged by some antiviruses.
Keep in mind that using any of these methods does not mean that Tekken Overlay does not contain any malicious code.
Using any of the methods above you are equally susceptible to anything that we could possibly put inside the `tekken-overlay.dll`.
At the end of the day you have to trust our team that we will not put anything malicious inside the `tekken-overlay.dll`.

### Linux Support

People have reported that the injector doesn't work on Linux and they keep getting the `Injecting DLL... FAIL!` error. [DeadAndRottingSite](https://www.reddit.com/user/DeadAndRottingSite) [have reported on reddit](https://www.reddit.com/r/Tekken/comments/rr7mlz/tekken_7_network_lag_fixes_play_online_with/hqm4uqs/) that you can do this to make it work on Linux:
* Use [Steam Tinker Launch](https://github.com/frostworx/steamtinkerlaunch). Install it depending on your distribution.
* Set Steam Tinker as a Steam compatibility tool: https://github.com/frostworx/steamtinkerlaunch/wiki/Steam-Compatibility-Tool.
* Set Tekken to run with it.
* Open its settings menu as it launches, and point a Custom Command to the TekkenOverlay executable, with Use Custom Command and Inject Custom Command settings (optionally a couple seconds wait time so the game launches first, shouldn't be necessary).

Donate
------

Special thanks to everyone who has contributed to this project. Over \$10000
worth of man hours has gone into this project to bring it to the tekken
community for free. A donation would be very much appreciated to keep the
project maintained and for potentially adding new features.  
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=tekkenoverlay%40gmail.com&currency_code=EUR)
