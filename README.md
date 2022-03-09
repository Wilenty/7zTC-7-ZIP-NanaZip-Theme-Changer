# 7zTC 2.0 (7-ZIP Theme Changer)

This program is much better version of this one: https://github.com/Wilenty/7-Zip-Theme-Manager-remake-of-version-2.1

**The changes are (and will be) described below the main program description.**

Now you can install 7-zip and apply any/all themes in one execution. Also, you can import theme(s) from installed/portable 7-zip as in 7zTM.

And it supports "a bit more" than 3 languages (about 70).
Some messages in the program are only in English, because they have not been translated in the InnoSetup.
The execution log is in English only, but some error messages can be in your OS/user language.
The working mode is also only in English, as for example "Apply Theme(s)" and "Import Theme", but I don't think these few phrases can be forgettable. Anyway, you can translate them from this text.

It will not "bumps" you with error messages (as 7zTM). I created first page with log from program loading, so, you can easily check themes files correction.

Because I saw that some users wrote that 7zTM did the work, but 7-zip theme(s) was not changed - it creates full log of script execution, which you will see on the last page (InnoSetup: Finished-Page) after execution (Apply/Import). There will be a "save" button, which allows you to save it (just in case).

In the execution log only the relative paths will be saved so, you will not need to edit it, if you will want to send the log to me (or someone else).
You can easily find the problems in the execution log, because all successful Exit-Codes are written as "(OK)" at the end of line. Other Error-Codes will be written as for example "(1)", "(5)", "(10)" or "(15)" and before the Error-Code you will see the OS message what failed.

Because only one person ( CrypticCus ) asked me to change the program colors (B/W), so, I didn't change the default InnoSetup colors.

**Changes in the program:**
## v2.0:
Added support for "NanaZip" ( big thanks to the chmichael user for good advice. Thank you so much! ).
But, I disabled the option to detect NanaZip installed from store, because it won't work (we don't have the write access rights there :]). So, it always failing with the message: "Access is denied (5)".

And since NanaZip does not support the "standard shell-extensions", I added the option to install/using 7-Zip with the NanaZip.dll (exactly the: "NanaZipCore.dll").
But, in my tests it works only with a "pure" (unmodified) 7z.dll from which the script copies all the needed resurces.
So, if you will see the error-code 13 "Bad data (13)" in the log file before/after the "Finishing update resource(s) of file (...)\NanaZipCore.dll" (the log its written in reverse order to speed-up the execution), it means that the Windows API can't update all of the resources, because it's too many of them...
In this case, you need to install 7-Zip along with the adding of NanaZip.dll, or you can try to copy the unmodified 7z.dll to the location of installed 7-Zip and then try again.

---

This program is shared as a Freeware (Donation-Ware).

Free version is available for free, but without command-line support. You can support me on Patreon ($5): https://www.patreon.com/posts/63191000
or Ko-Fi (5€): https://ko-fi.com/Wilenty
to get your personal version with command-line support.

Please provide in message the nickname or e-mail, or (if you want) the first name and second name, for who the program will be designed?

Multi-license (business) version are also available, please contact me personally with your offer.

P.S.
**Please, don't share your personal version in the internet.
I will share for all supporters the fixed version, if there will be any errors in the program. But, if I can find your personal version in the internet - then I will not share the version without bugs for you.**
