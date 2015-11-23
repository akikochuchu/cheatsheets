##iOS Remote Debugging with LLDB

Mount the DeveloperDiskImage.dmg:
```
hdiutil attach /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/DeviceSupport/8.0\ \(12A365\)/DeveloperDiskImage.dmg
```

Copy the ```debugserver``` locally: 
```
cp /Volumes/DeveloperDiskImage/usr/bin/debugserver /Users/rotlogix/
```

Create a new ```entitlements.plist```:
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/ PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>com.apple.springboard.debugapplications</key> <true/>
    <key>run-unsigned-code</key>
    <true/>
    <key>get-task-allow</key>
    <true/>
    <key>task_for_pid-allow</key>
    <true/>
</dict>
</plist>
```

Sign the ```debugserver```:
```
codesign -s - --entitlements entitlements.plist -f debugserver
```

Attack the ```debugserver``` to a process:
```
debugserver *:6666 --attach SomeApplication
```

Attach LLDB to the remote ```debugserver```:
```
(lldb) platform select remote-ios
(lldb) process connect connect://192.168.0.8:6666
```

Create target from executable:
```
(lldb) target create --arch arm main
```
