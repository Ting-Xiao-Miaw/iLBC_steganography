# iLBC_steganography

## Build up
[PJSUA](https://www.pjsip.org/pjsua.htm)
1. Download [PJSIP source code](https://www.pjsip.org/download.htm) (Version 2.13).
2. Open pjproject-vs14.sln with Visual Studio 2019.
3. Do not recover the solution file.
4. Right-click the solution and select "Re-target Solution".
5. Customize config_site.h
6. Modify "pjlib/include/pj/config_site.h"
7. #include <pj/config_site_sample.h>
8. Right-click the project "pjsua" and select "Set as Startup Project".
9. Right-click the project "pjsua" and select "Build". (Please make sure your mode is "Debug" and "Win32". It cannot be "Any".)
10. After all the projects are built successfully, you can find "pjsua-i386-Win32-vc14-Debug.exe" under "pjproject-2.13/pjsip-apps/bin". This file can be copied to another Windows PC and executed directly.

## Replace file
1. Replace "iLBC_encoder.c", "iLBC_decoder.c" and "iLBC_define.h" under "pjproject-2.13.1/third_party/ilbc" with the code we provide.
2. Move "sharedBuffer.c" and "sharedBuffer.h" under "pjproject-2.13.1/third_party/ilbc".
