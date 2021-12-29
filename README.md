Tekken Overlay
==============

This software is intended for educational purposes only. The software is not to
be used to gain competetive advantage. We take no responsibility for misuse of
this software in a competitive setting.

How to use
-------

Download and install VC++ 2015-2019 Redistributables(vc_redist.x64.exe file) from [here](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads).  
Download Tekken Overlay
[here​​​](https://github.com/TekkenOverlay/TekkenOverlay/releases/latest)(Download the top .zip file).
Extract zip to anywhere.  
Run tekken-overlay-run.exe.  
Run Tekken.

Problems
--------

### Injecting DLL... FAIL!

#### Reason #1

This might mean you haven’t extracted .zip archive and running your *tekken-overlay-run.exe* file
from inside the .zip archive. Extract your .zip archive as instructed in the
[Install section](https://github.com/TekkenOverlay/TekkenOverlay#install) and
then run the *tekken-overlay-run.exe* file.

#### Reason #2

Another reason you can get this error is because of VC++ Redistributables installed on your machine. Install VC++ Redistributables 2015-2019 from [here](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads). This should fix the `Injecting DLL... FAIL!` error.

### Not working overlay

If framedata and/or hitboxes don't show up but game information and throw counter work, check that your rendering scale is set to 100.
Tekken 7 Main menu -> Settings -> Graphics Settings -> Rendering Scale -> Set to 100

Donate
------

Special thanks to everyone who has contributed to this project. Over \$10000
worth of man hours has gone into this project to bring it to the tekken
community for free. A donation would be very much appreciated to keep the
project maintained and for potentially adding new features.  
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=tekkenoverlay%40gmail.com&currency_code=EUR)
