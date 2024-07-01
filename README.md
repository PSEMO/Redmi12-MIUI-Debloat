# Redmi12-MIUI-Debloat

This is an guide on how to debloat your Redmi 12 phone using Linux

<h2>---SETUP---</h2>
<p>
Linux setup:
$ sudo apt-get install android-tools-adb

Setup your Xiaomi Phone:
Enable Developer options > go to developer options > enable "USB debugging"
</p>
<h2>---COMMANDS---</h2>

shows all connected adb devices
$ adb devices

launches a shell on the device
$ adb shell

reboots the device
$ adb reboot

list all packages on the device
$ adb shell pm list packages

installs the given .apk file to the device
$ adb install "filename"

<h2>---GUIDE---</h2>

This will show installed packages
$ adb shell pm list packages

This is the uninstall command
$ adb uninstall [package name]
You should use this one if the above does not work and you get "internal error"
$ adb shell pm uninstall --user 0 [package name]

This will uninstall packages I've picked out
$ adb uninstall com.google.android.apps.docs; adb uninstall com.google.android.apps.photos; adb uninstall com.google.android.apps.tachyon; adb uninstall com.google.android.apps.wellbeing; adb uninstall com.google.android.videos; adb uninstall com.miui.msa.global; adb uninstall com.miui.analytics; adb uninstall com.miui.android.fashiongallery; adb shell pm uninstall --user 0 com.miui.backup; adb uninstall com.miui.bugreport; adb uninstall com.miui.cloudbackup; adb shell pm uninstall --user 0 com.miui.cloudservice; adb shell pm uninstall --user 0 com.miui.micloudsync; adb uninstall com.miui.fm; adb shell pm uninstall --user 0 com.miui.fmservice; adb shell pm uninstall --user 0 com.miui.freeform; adb shell pm uninstall --user 0 com.miui.misound; adb shell pm uninstall --user 0 com.miui.miwallpaper; adb shell pm uninstall --user 0 com.miui.qr; adb shell pm uninstall --user 0 com.xiaomi.calendar ; adb shell pm uninstall --user 0 com.xiaomi.discover; adb shell pm uninstall --user 0 com.xiaomi.glgm; adb shell pm uninstall --user 0 com.xiaomi.mipicks; adb shell pm uninstall --user 0 com.facebook.appmanager; adb shell pm uninstall --user 0 com.facebook.services; adb shell pm uninstall --user 0 com.facebook.system; adb shell pm uninstall --user 0 com.duokan.phone.remotecontroller; adb reboot
