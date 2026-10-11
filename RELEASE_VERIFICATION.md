# Release verification — FF Bio Code v1.0.0

This record describes the APK attached to the [v1.0.0 GitHub release](https://github.com/ayan-act/FF-Bio-Code/releases/tag/v1.0.0). Values were read from the published APK on 11 October 2026 using Android SDK Build Tools; the file's SHA-256 matched GitHub's release-asset digest. This is an artifact check, not a source-code audit or a claim that every app feature has been runtime tested.

| Property | Verified value |
| --- | --- |
| Asset | `app-release.apk` |
| Size | 3,822,836 bytes |
| SHA-256 | `70709e6f0a804a835bdf0f79e1e67d709666cd4497cef2aa76a661f1e49d600d` |
| Application ID | `com.ffbiocodes.app` |
| Version | `versionName=1.0.0`, `versionCode=1` |
| Minimum Android | API 24 (Android 7.0) |
| Target Android | API 35 (Android 15) |
| Signing certificate SHA-256 | `5034f3b429ec4fee2978bb4b00a625b7e49dfcbd3f28745d6a455760e919feeb` |

## Check a downloaded APK

Download the asset from the [official release](https://github.com/ayan-act/FF-Bio-Code/releases/tag/v1.0.0). In PowerShell, run:

```powershell
(Get-FileHash -Algorithm SHA256 -LiteralPath .\app-release.apk).Hash.ToLowerInvariant()
```

Compare the result with the SHA-256 value above. With Android SDK Build Tools installed, `apksigner verify --print-certs app-release.apk` can verify the APK signature and display the public signing-certificate fingerprint. Never publish the private signing key or keystore.

## Permissions declared in this APK

The manifest declares these permissions; presence in the manifest alone does not establish when a permission is used or what data is collected:

- Network and background operation: `INTERNET`, `ACCESS_NETWORK_STATE`, `WAKE_LOCK`, `FOREGROUND_SERVICE`.
- Notifications and messaging: `POST_NOTIFICATIONS`, `com.google.android.c2dm.permission.RECEIVE`.
- Advertising-related: `com.google.android.gms.permission.AD_ID`, `ACCESS_ADSERVICES_AD_ID`, `ACCESS_ADSERVICES_ATTRIBUTION`, `ACCESS_ADSERVICES_TOPICS`.
- App-specific receiver permission: `com.ffbiocodes.app.DYNAMIC_RECEIVER_NOT_EXPORTED_PERMISSION`.

See the website's [privacy policy](https://ffbiocodes.com/privacy-policy/) for its published data-handling information. Review the app and included SDK behavior before making more specific privacy claims.

## Next release

Recompute the APK checksum, certificate fingerprint, version values, permissions, and supported Android versions for each new release. Update this document and the README together. Keep release notes tied to the actual build and test results.
