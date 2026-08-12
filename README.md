# Cordova APP Builder
 
Build a branded Android APK from any website using GitHub Actions — no local setup required.
 
## Steps to build a new APP
 
1. Replace the app icon in the `/res` folder with your own icon file named exactly `icon.png`.
2. Fill in the app's repository secrets under **Settings → Secrets and variables → Actions**.
3. Go to the **Actions** tab, choose **Build Android APK**, open the **Run workflow** dropdown, and click **Run workflow**.
4. After the run succeeds, download the APK from the **Artifacts** section of the workflow run.
## Repository secrets
 
| Secret | Example | Required |
|---|---|:---:|
| `APP_NAME` | `7LUCK88` | Yes |
| `PACKAGE_ID` | `com.sevenluck88.app` | Yes |
| `TARGET_URL` | `https://7luck88.co?isApp=1` | Yes |
| `VERSION_NAME` | `1.0.1` | Yes |
| `VERSION_CODE` | `1` | Yes |
| `ORIENTATION` | `default` \| `portrait` \| `landscape` | No |
 
**Notes**
 
- `PACKAGE_ID` must be a valid Android application id: each dot-separated segment must start with a letter and contain only letters, digits, or underscore — no leading digit, hyphen, space, or non-ASCII character. This is why the `7LUCK88` brand uses `com.sevenluck88.app` rather than `com.7luck88.app`.
- `VERSION_CODE` is an integer build number; increase it by 1 for every release you upload.
- `ORIENTATION` is optional. Omit it or use `default` to allow rotation; use `portrait` or `landscape` to lock the app.
