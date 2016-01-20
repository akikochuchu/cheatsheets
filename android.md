##Convert ODEX to DEX

```java -jar baksmali.jar -d /system/framework -x app.odex```

```java -jar smali.jar -o classes.dex out/```

```java -jar oat2dex.jar boot /system/framework/arm/boot.oat```

### Lollipop

```
java -jar oat2dex.jar ~/samsung-j1/app/AllshareFileShare/arm/AllshareFileShare.odex ~/samsung-j1/framework/arm/odex
```

##Find CodePath for Target Package

```adb shell "su -c 'cat /data/system/packages.xml'" | grep 'com.sec.android.mmapp' | grep 'codePath=*'```

## Create JNI Headers (OS X)
```
javah -v -classpath ~/Library/Android/sdk/platforms/android-18/android.jar:./build/intermediates/classes/debug/ com.rotlogix.sprayandspray.services.FileParserService
```

## BKS
```
keytool -importcert -v -trustcacerts -file /Users/benjaminwatson/Tools/web/burp/burp.cer -providerpath /Users/benjaminwatson/Downloads/bcprov-jdk15on-152.jar -provider org.bouncycastle.jce.provider.BouncyCastleProvider -storetype BKS -keystore ~/Downloads/com.onlycoin.android-1/assets/coincert.bks 
```
