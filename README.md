# Andoukie (doukie client for Android)

doukie client for Android. ([what is doukie? here](https://github.com/yasutakatou/doukie).)

# solution

AirDrop is very useful file transfer method.<br>
But, It's not what I'd expect opened economy method.<br>
on not supported computers, is require support by official or OSS comunity effort.<br>
<br>
**We know universal protocol, is HTTP.**<br>
<br>
I think to want implement easy file transfer method by HTTP.<br>
and, I realize file transfer on multi platform **(include Smart phone!)**.

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

[or download binary from release page](https://github.com/yasutakatou/andoukie/releases).<br>
save binary file, and adb install.

```
adb install (place of adb file.)
```

# uninstall

use app uninstall method on Android.

# method of operation

 - 1st

![1](https://github.com/yasutakatou/andoukie/blob/pic/1.png)

run doukie on you want to sync device.<br>
after running, enter key or space key on terminal console.<br>
QR Code displaying.<br>
run this app on Android, and read to QR Code.<br>

 - 2nd

operating on Android touch pannel.<br>

![2](https://github.com/yasutakatou/andoukie/blob/pic/2.png)

① not delete mode

default this switch is off.<br>
If some file exists Android, but not exists server, that file delete on .<br>
when turn on this switch to not delete.<br>

② gauge of sync interval

this gauge is interval of file syncing.<br>
example (60), is sync every 60 seconds.<br>
(0) is not syncing.<br>

③ status column

This place display sync status or another message.<br>

# problem

- why Android can't use server and auto sync mode?<br>

this application builed by Apache Cordova.<br>
Cordova plugins are very instability.<br>
I can't work to want any features.<br>
(I feel about 50% not work. because depend old Android API.)<br>
By the next try to build Android application, I consider another framework, react native, Flutter..<br>

- where save synced files?<br>

Internal Storage<br>
	- Android<br>
		- data<br>
			- io.cordova.hellocordova<br>
				- files<br>

- why static save location?<br>

As I wrote earlier. cordova plugin not work.<br>
example) https://github.com/ourcodeworld/cordova-ourcodeworld-filebrowser<br>
and I don't know how for implementetion.<br>
If you teach to me this implement, I would coding.<br>

# FYI (many thanks!)

 - on and off, toggle switch<br>
https://www.w3schools.com/howto/howto_js_toggle_hide_show.asp

 - gauge for sync duration<br>
https://github.com/andrepxx/pure-knob

 - file exists check<br>
https://stackoverflow.com/questions/10294166/how-to-check-a-files-existence-in-phone-directory-with-phonegap/13333136#13333136

 - save blog data to binary file<br>
https://ourcodeworld.com/articles/read/230/how-to-save-a-pdf-from-a-base64-string-on-the-device-with-cordova

 - file remove<br>
https://stackoverflow.com/questions/33752990/cordova-remove-file

 - get file list<br>
https://stackoverflow.com/questions/28937878/cordova-list-all-files-from-application-directory-www

 - popup<br>
https://www.w3schools.com/howto/howto_js_popup.asp
