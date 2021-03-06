---
layout: post
title: Dual signing Windows software
---
Starting in January 2016, Windows 7 and newer no longer trust new software signed using SHA-1 certificates. This means developers will need to sign new binaries, INFs and MSIs with SHA256 certificates and time stamps.

<!--more-->

[![Online security by Danny Oosterveer]({{ site.baseurl }}/images/cc-locks.jpg) "Online security by Danny Oosterveer (CC BY-ND 2.0)"](https://www.flickr.com/photos/dannyoosterveer/7913182734)

Unfortunately, Windows XP does not recognize SHA256 certificates or time stamps. This puts us in a bit of a bind. Luckily, you can handle this issue by dual signing your binaries and INFs. MSIs cannot be dual signed, though. I haven't figured out a solution to this issue yet. Currently, I just distribute two MSIs with different signatures.

### Dual Signing Files ###

First, I like to add the Windows Kit bin directory to my path. I use these tools often, including signtool.exe needed for signing files: C:\Program Files (x86)\Windows Kits\8.1\bin\x64

I have an extended validation signing token. This requires some middleware to verify the dongle and prompts for my password. Signtool will automatically try to find the best possible certificate but if you simply have a .pfx file, add it using /f and /p for the password. My EV token requires the MSCV-VSClass3.cer file to be added in using the /ac flag.

    signtool sign /ac MSCV-VSClass3.cer /t http://timestamp.verisign.com/scripts/timstamp.dll /v "file.exe"
    signtool sign /ac MSCV-VSClass3.cer /fd SHA256 /tr http://timestamp.globalsign.com/?signature=sha2 /td SHA256 /as /v "file.exe"

The first command signs using SHA1 and the second signs using SHA256. The /as flag tells signtool to append the second signature and not overwrite the first signature.

I also recommend verifying the signature afterwards using the following command:

    signtool verify /pa /all "file.exe"

If this command lists two valid signatures, your software will be signed and ready to distribute.
