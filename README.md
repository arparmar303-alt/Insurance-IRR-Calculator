# Insurance IRR Calculator — Android project

This Android Studio project wraps the calculator in an offline WebView app.
The app name is **Insurance IRR Calculator** and the application ID is
`com.insuranceirr.calculator`.

## Build an APK with Android Studio

1. Install Android Studio on a computer.
2. Choose **Open** and select this project folder.
3. Allow Gradle sync to complete. The first build requires internet access to
   download Android Gradle Plugin dependencies and Android SDK components.
4. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. Android Studio will show a notification with a link to the generated APK.
   For a debug build, it is usually at `app/build/outputs/apk/debug/app-debug.apk`.

## Install on your Android phone

Transfer `app-debug.apk` to your phone and open it. Android may ask you to allow
installation from that file manager; only enable this for the file you built
yourself. For wider distribution, create a signed release APK from Android Studio.

## Notes

- The calculator is bundled locally and works offline.
- It does not request internet, contacts, location, or storage permissions.
- This source package is not itself an APK; an Android SDK/build environment is
  required to compile and sign the installable APK.


## Build APK from an Android phone using GitHub Actions (no computer)

This project includes `.github/workflows/android-apk.yml` for a cloud build.

1. In your phone browser, create/sign in to a GitHub account at https://github.com.
2. Create a **new private repository** named `InsuranceIRRCalculator`.
3. Upload the contents of this ZIP to the repository (extract ZIP first if GitHub's mobile upload page cannot handle folders).
4. Open the repository's **Actions** tab and enable workflows if prompted.
5. Select **Build Insurance IRR Calculator APK**, tap **Run workflow**, then open the completed run.
6. Under **Artifacts**, download `Insurance-IRR-Calculator-APK` and extract it to get `app-debug.apk`.
7. Open the APK on your phone to install. Android may ask you to allow installs from your browser or file manager.

The workflow builds a **debug APK** suitable for personal testing. GitHub requires a signed-in account, and its Actions UI can be awkward on mobile. Do not share GitHub passwords or access tokens in chat. Only upload this calculator source project, not customer or policy data.
