# README

- Host webapp/examplecorp folder with PHP under a domain, this acts as `ad.com`
    - we've used `examplecorp.de`
    - We have used apache and PHP 8.2
    - Exchange the encryption key in L2 of `util.php` 
- Optionally: To test web tracking host webapp/ravioli under a different domain
    - we've used `schnellnochraviolimachen.de`  

## Build Apps:
- Install Android Studio
- Open apps in Android Studio
- If not already present: Generate release keys and adjust `build.gradle` accordingly.
    - https://developer.android.com/studio/publish/app-signing
- Adjust domains in DALs in the app, at both `app/src/main/res/values/strings.xml`
- Adjust domains in source of the app, replace `examplecorp.de` at both `app/src/main/res/layout/fragment_first.xml`
- Adjust release keys for DALs in the `.well-known` folder of the webapp(s)
    - Refer to https://developer.android.com/training/app-links/verify-android-applinks#web-assoc 
- Build both apps
    - The `build.gradle` builds the regular (developer) build with release keys, i.e. DALs and therefore TWAs work without explicitly building a release

## Test
- Follow steps in demo or play around
