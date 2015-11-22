##Convert ODEX to DEX

```java -jar baksmali.jar -d /system/framework -x app.odex```

```java -jar smali.jar -o classes.dex out/```

##Find CodePath for Target Package

```adb shell "su -c 'cat /data/system/packages.xml'" | grep 'com.sec.android.mmapp' | grep 'codePath=*'```
