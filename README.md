# 7zTC v3.0.1 (7-ZIP/NanaZip Theme Changer)

[![Latest Version](https://img.shields.io/github/release/Wilenty/7zTC-7-ZIP-NanaZip-Theme-Changer.svg)](https://github.com/Wilenty/7zTC-7-ZIP-NanaZip-Theme-Changer/releases/latest)
[![Total Downloads](https://img.shields.io/github/downloads/Wilenty/7zTC-7-ZIP-NanaZip-Theme-Changer/total.svg)](https://github.com/Wilenty/7zTC-7-ZIP-NanaZip-Theme-Changer/releases)
[![Latest Release Downloads](https://img.shields.io/github/downloads/Wilenty/7zTC-7-ZIP-NanaZip-Theme-Changer/latest/total.svg)](https://github.com/Wilenty/7zTC-7-ZIP-NanaZip-Theme-Changer/releases/latest)
[![v3.0.1 Release Downloads](https://img.shields.io/github/downloads/Wilenty/7zTC-7-ZIP-NanaZip-Theme-Changer/v3.0.1/total.svg)](https://github.com/Wilenty/7zTC-7-ZIP-NanaZip-Theme-Changer/releases/tag/v3.0.1)

This program is much better version of this one: https://github.com/Wilenty/7-Zip-Theme-Manager-remake-of-version-2.1

**The changes are (and will be) described below the main program description.**

Now you can install 7-zip and apply any theme in one execution. Also, you can import theme(s) from installed/portable 7-zip as in 7zTM.

And it supports "a bit more" than 3 languages (about 70).
Some messages in the program are only in English, because they have not been translated in the InnoSetup.
The execution log is in English only, but some error messages can be in your OS/user language.
The working mode is also only in English, as for example "Apply Theme(s)" and "Import Theme", but I don't think these few phrases can be forgettable. Anyway, you can translate them from this text.

It will not "bumps" you with error messages (as 7zTM). I created first page with log from program loading, so, you can easily check themes files correction.

Because I saw that some users wrote that 7zTM did the work, but 7-zip theme(s) was not changed - it creates full log of script execution, which you will see on the last page (InnoSetup: Finished-Page) after execution (Apply/Import). There will be a "save" button, which allows you to save it (just in case).

In the execution log only the relative paths will be saved so, you will not need to edit it, if you will want to send the log to me (or someone else).
You can easily find the problems in the execution log, because all successful Exit-Codes are written as "(OK)" at the end of line. Other Error-Codes will be written as for example "(1)", "(5)", "(10)" or "(15)" and before the Error-Code you will see the OS message what failed.

Because only one person ( CrypticCus ) asked me to change the program colors (B/W), so, I didn't change the default InnoSetup colors.

## Changes in the program:

<details><summary>v2.0:</summary>

Added support for "NanaZip" ( big thanks to the chmichael user for good advice. Thank you so much! ).
But, I disabled the option to detect NanaZip installed from store, because it won't work (we don't have the write access rights there :]). So, it always failing with the message: "Access is denied (5)".

Get the latest installer (*.msixbundle) of NanaZip from there: https://github.com/M2Team/NanaZip/releases/latest
In my program select the NanaZip, then select the *.msixbundle for installation in "Install NanaZip?" - it will extract the correct files into selected location for installation, and will be able to modify the resources.

And since NanaZip does not support the "standard shell-extensions", I added the option to install/using 7-Zip with the NanaZip.dll (exactly the: "NanaZipCore.dll").
But, in my tests it works only with a "pure" (unmodified) 7z.dll from which the script copies all the needed resurces.
So, if you will see the error-code 13 "Bad data (13)" in the log file before/after the "Finishing update resource(s) of file (...)\NanaZipCore.dll" (the log its written in reverse order to speed-up the execution), it means that the Windows API can't update all of the resources, because it's too many of them...
In this case, you need to install 7-Zip along with the adding of NanaZip.dll, or you can try to copy the unmodified 7z.dll to the location of installed 7-Zip and then try again.

</details>

---

<details><summary>v2.1:</summary>

Note: before use this version, please delete the folder of extracted NanaZip, if you used it with version 2.0, usually "C:\Program Files\NanaZip". Now my program extracts only the files needed for standard APP's, without unneeded store stuff.

Added shell-extensions for NanaZip ( big thanks to the chmichael user for the motivation! :) ). Also, it assigns all the file-types extension to the NanaZip, so, now it works out-of-the-box. My program creates uninstall section of extracted NanaZip, so, it can be easily uninstalled.

On installing NanaZip please select your favorite theme of file-types, but if you don't select any, script chooses the first one from the list which usually is the "Default 7-Zip theme" for file-types.

BTW, I forgot to write before that it should also work on ARM64 Systems, with exceptions of shell-extensions and file-types, because VS2015CE does not support ARM64 architecture. :]

</details>

---

<details><summary>v2.2:</summary>

Fixed NanaZip Installing and Mixed-Install, from now it can work a bit slower on these two, but a way better. It should correctly add the file-types without any errors about "Bad data (13)".

Added the "windows_11_theme_for_7_zip_by_ivan13x_demykcf" from there: https://sourceforge.net/p/sevenzip/discussion/45797/thread/d82ec82a71/

</details>

---

<details><summary>v2.2.1:</summary>

Fixed installation of latest version of NanaZip (v1.2.252.0).

(2022-05-14 {YYYY-MM-DD})

At the request of user Patrxgt added the following themes:
```
\---ToolBar
    +---Office 2013
    +---Windows 10 Blue
    +---Windows 10 Default
    +---Windows 10 Modern
```
Thanks!

And added the following themes from there: https://github.com/RipplePiam/7zip-Theme
```
\---Filetype
   +---Windows 10 Blue
   +---Windows 10 Default
\---ToolBar
    +---Glyfz 2016
```

</details>

---

<details><summary>v2.5:</summary>

Created comfortable installer to extract or launch the program - added some example files (*.cmd) to extract or launch, and described all parameters in *.txt files. Now you can extract only the program, or immediately launch it with selected themes, also you can create your own collection of the themes by extracting only those which you want to use.

Restored the possibility to change themes of NanaZip installed via store, after positive reports that if works without any problems. But I disabled auto-detecting of NanaZip installed via store in 7zTC.
I am still not responsible for any damage done to the store - you doing it at your own risk.

</details>

---

**v3.0(.1):**

Now it should works with "NanaZip 1.0 Preview 1 (1.0.25.0)" from there: https://github.com/M2Team/NanaZip/releases?page=3
up to "NanaZip 3.0 Preview 0 (3.0.756.0)" from there: https://github.com/M2Team/NanaZip/releases?page=1
And in any future versions, if they don't change the file-names in the future :]

Added (optional) icon "apfs.ico" which can be found in: FileType\7-Zip Original Theme\apfs.ico

**v3.0.1**: Small fix for "some times doesn't install at all because it says theres 2 of the same programs open, both happens on win 10&11"
https://github.com/Wilenty/7zTC-7-ZIP-NanaZip-Theme-Changer/issues/11

---

This program is shared as a Donation-Ware (Freeware).

P.S.
**Please, don't share your personal version in the internet.
I will share for all supporters the fixed version, if there will be any errors in the program. But, if I can find your personal version in the internet - then I will not share the version without bugs for you.**
