# Andoukie (doukie client for Android)

doukie client for Android. (what is doukie? here.)

# solution

AirDrop is very useful file transfer method.
But, It's not what I'd expect opened economy method.
on not supported computers, is require support by official or OSS comunity effort.

We know universal protocol, is HTTP.
I think to want implement easy file transfer method by HTTP.
and, I realize file transfer on multi platform (include Smart phone!).

# features

 - read QR Code to syncing (no input operation)
 - gauge and switch easily operation
 - file exists check (use md5 hash)

# installation

manually install

```
git clone https://github.com/yasutakatou/andoukie
cd andoukie
cordova platform add android
cordova build android
(displaying place of adb file.)
adb install (place of adb file.)
```

[or download binary from release page]().
save binary file, and adb install.

```
adb install (place of adb file.)
```

# uninstall

use app uninstall method on Android.

# method of operation

 - 1st

run doukie on you want to sync device.
after running, enter key or space key on terminal console.
QR Code displaying.
run this app on Android, and read to QR Code.

 - 2nd

operating on Android touch pannel.

① not delete mode

default this switch is off.
If some file exists Android, but not exists server, that file delete on .
when turn on this switch to not delete.

② gauge of sync interval

this gauge is interval of file syncing.
example (60), is sync every 60 seconds.
(0) is not syncing.

③ status column

This place display sync status or another message.

# problem

- why Android can't use server and auto sync mode?

this application builed by Apache Cordova.
Cordova plugins are very instability.
I can't work to want any features.
(I feel about 50% not work. because depend old Android API.)
By the next try to build Android application, I consider another framework, react native, Flutter..

- where save synced files?

Internal Storage
	- Android
		- data
			- io.cordova.hellocordova
				- files

- why static save location?

As I wrote earlier. cordova plugin not work.
example) https://github.com/ourcodeworld/cordova-ourcodeworld-filebrowser
and I don't know how for implementetion.
If you teach to me this implement, I would coding.

# FYI (many thanks!)

 - on and off, toggle switch
https://www.w3schools.com/howto/howto_js_toggle_hide_show.asp

 - gauge for sync duration
https://github.com/andrepxx/pure-knob

 - file exists check
https://stackoverflow.com/questions/10294166/how-to-check-a-files-existence-in-phone-directory-with-phonegap/13333136#13333136

 - save blog data to binary file
https://ourcodeworld.com/articles/read/230/how-to-save-a-pdf-from-a-base64-string-on-the-device-with-cordova

 - file remove
https://stackoverflow.com/questions/33752990/cordova-remove-file

 - get file list
https://stackoverflow.com/questions/28937878/cordova-list-all-files-from-application-directory-www

 - popup
https://www.w3schools.com/howto/howto_js_popup.asp
