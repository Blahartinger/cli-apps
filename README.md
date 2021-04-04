# cli-apps

## Zero warranty or help available for this right now. Use at your own risk, DYOR, or build something with it.
Currently contains an app that can be used to parse the data from a kin qr code of the following format using libSodium.
NOTE: libSodium must be on the path for the utility to work.
```json
{
    "pKey": "XXXXX",
    "seed": "YYYY",
    "salt": "ZZZZ"
}
```

To use to parse out a private key:
`java -jar cli-app/build/libs/cli-app.jar import <string escaped json data> <password used to encrypt seed>`

To export a private key into qr code json data format:
`java -jar cli-app/build/libs/cli-app.jar export <private key string> <password to encrypt seed>`

Optionally, to add libSodium to your classpath include this in your command:
```
-Djava.library.path=/usr/local/lib
```
Prebuilt MacOS and linux binaries available here `https://github.com/kinecosystem/kin-android/tree/master/jniLibs/macOS`
