# Android Development

## Install Android Studio

Download Android Studio from this link: [Android Studio](https://developer.android.com/studio)

Then, create the application directory:

```
mkdir -p ~/Applications/AndroidStudio
```

Then, copy the tar and unpack it:

```
cp ~/Downloads/android-studio-*.tar.gz ~/Applications/AndroidStudio
tar xvf ~/Applications/AndroidStudio/android-studio-*.tar.gz -C ~/Applications/AndroidStudio
rm ~/Applications/AndroidStudio/*.tar.gz
```

Then symlink it to the `latest` directory:

```
ln -s ~/Applications/AndroidStudio/android-studio ~/Applications/AndroidStudio/latest
```

Then, run the app: `~/Applications/AndroidStudio/latest/studio.sh`, and go through the setup wizard.

Look into hardware acceleration at this link: [Hardware Acceleration](https://developer.android.com/studio/run/emulator-acceleration?utm_source=android-studio#vm-linux)

This is a bit complicated... come back to it.

Don't forget to create desktop entry.