# harvest_app

## Build
Run `flutter build apk` (for Android) or `flutter build ios` (for iOS).

## Todo
### Disable HTTP
Currently, HTTPS is not available, only HTTP. So the following lines are added to enable it:
In `android/app/src/main/AndroidManifest.xml`:
`android:usesCleartextTraffic="true"`

In `ios/Runner/Info.plist`:
```
<key>NSAppTransportSecurity</key>
<dict>
	<key>NSAllowsArbitraryLoads</key>
	<true/>
</dict>
```

Remove these lines after HTTPS is available and no HTTP is needed.