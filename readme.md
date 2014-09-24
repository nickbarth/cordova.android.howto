How to Android Cordova

Setup
```
  cordova platform add android

```

Plugins

```
  cordova plugin add org.apache.cordova.camera
  cordova plugin add org.apache.cordova.console
  cordova plugin add org.apache.cordova.device
  cordova plugin add org.apache.cordova.file
  cordova plugin add org.apache.cordova.file-transfer
  cordova plugin add org.apache.cordova.media
  cordova plugin add org.apache.cordova.media-capture
  cordova plugin add org.apache.cordova.network-information
  cordova plugin add org.apache.cordova.splashscreen
  cordova plugin add org.apache.cordova.statusbar

  # Requires Manual Install https://github.com/Wizcorp/phonegap-facebook-plugin/blob/master/platforms/android/README.md#setup-without-eclipse-just-cli
  cordova plugin add com.phonegap.plugins.facebookconnect --variable APP_ID="APP_ID" APP_NAME="APP"
```

```
  # platforms/android/AndroidManifest.xml
  <uses-sdk android:minSdkVersion="10" android:targetSdkVersion="19" />
  <uses-permission android:name="android.permission.INTERNET" />
  <uses-permission android:name="android.permission.RECORD_AUDIO" />
  <uses-permission android:name="android.permission.MODIFY_AUDIO_SETTINGS" />
  <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
  <uses-permission android:name="android.permission.READ_PHONE_STATE" />
  <uses-permission android:name="android.permission.BROADCAST_STICKY" />
  <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
  <uses-permission android:name="android.permission.VIBRATE" />
```

```
  # platforms/android/res/xml/config.xml
  <plugin name="File" value="org.apache.cordova.FileUtils" />
  <plugin name="FileTransfer" value="org.apache.cordova.FileTransfer" />
  <plugin name="Capture" value="org.apache.cordova.Capture"/>
  <plugin name="Device" value="org.apache.cordova.Device" />
  <plugin name="Battery" value="org.apache.cordova.BatteryListener" />
  <plugin name="InAppBrowser" value="org.apache.cordova.InAppBrowser" />
  <plugin name="Media" value="org.apache.cordova.AudioHandler" />
  <plugin name="Notification" value="org.apache.cordova.Notification"/>
  <plugin name="SplashScreen" value="org.apache.cordova.SplashScreen"/>
  <plugin name="Storage" value="org.apache.cordova.Storage" />
```

```
  # Generate Hash and Add Android Platform to Facebook
  # See https://developers.facebook.com/docs/android/getting-started#create-app
  # Use Something LIKE this
  keytool -exportcert -alias androiddebugkey -keystore/.android/debug.keystore | openssl sha1 -binary | openssl base64
```

&copy; 2014 MIT Nick Barth
