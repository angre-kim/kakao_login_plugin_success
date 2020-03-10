# flutterkakaologin0310_not SDK but plugin

1. `kakao_strings.xml`를

```<?xml version="1.0" encoding="utf-8"?>
<resources>
    <string name="kakao_app_key">XXXX</string>
</resources>
```
2. `Androidmanifest.xml`를

 ```<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.angre.flutterkakaologin0310">
    <!-- io.flutter.app.FlutterApplication is an android.app.Application that
         calls FlutterMain.startInitialization(this); in its onCreate method.
         In most cases you can leave this as-is, but you if you want to provide
         additional functionality it is fine to subclass or reimplement
         FlutterApplication and put your custom class here. -->
   ** <uses-permission android:name="android.permission.INTERNET"/>**
    <application
        android:name="io.flutter.app.FlutterApplication"
        android:label="flutterkakaologin0310"
        android:icon="@mipmap/ic_launcher">

        <activity
            android:name=".MainActivity"
            android:launchMode="singleTop"
            android:theme="@style/LaunchTheme"
            android:configChanges="orientation|keyboardHidden|keyboard|screenSize|smallestScreenSize|locale|layoutDirection|fontScale|screenLayout|density|uiMode"
            android:hardwareAccelerated="true"
            android:windowSoftInputMode="adjustResize">
            <intent-filter>
                <action android:name="android.intent.action.MAIN"/>
                <category android:name="android.intent.category.LAUNCHER"/>
            </intent-filter>
        </activity>
        <!-- Don't delete the meta-data below.
             This is used by the Flutter tool to generate GeneratedPluginRegistrant.java -->
        <meta-data
            android:name="flutterEmbedding"
            android:value="2" />
      **  <meta-data
            android:name="com.kakao.sdk.AppKey"
            android:value="@string/kakao_app_key" />**
    </application>
</manifest>```
