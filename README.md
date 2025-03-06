# Repro for issue 8293

## Versions

node: v20.9.0<br>
firebase-tools: v13.32.0

```
$ flutter --version
Flutter 3.24.0 • channel stable • https://github.com/flutter/flutter.git
Framework • revision 80c2e84975 (7 months ago) • 2024-07-30 23:06:49 +0700
Engine • revision b8800d88be
Tools • Dart 3.5.0 • DevTools 2.37.2
```

## Steps to reproduce

1. Run `flutter pub get`
1. Run `firebase deploy`
1. See outputs below with using firebase-tools v13.32.0 and v13.31.2

### 13.32.0

Run `firebase deploy --only hosting:aalej-test-site --project PROJECT_ID`

```
$ firebase deploy --only hosting:aalej-test-site --project PROJECT_ID

=== Deploying to 'PROJECT_ID'...

i  deploying hosting
i  hosting[aalej-test-site]: no "public" directory to upload, continuing with release
i  hosting[aalej-test-site]: finalizing version...
✔  hosting[aalej-test-site]: version finalized
i  hosting[aalej-test-site]: releasing new version...
✔  hosting[aalej-test-site]: release complete

✔  Deploy complete!
```

### 13.31.2

Run `firebase deploy --only hosting:aalej-test-site --project PROJECT_ID`

```
$ firebase deploy --only hosting:aalej-test-site --project PROJECT_ID

   Thank you for trying our experimental support for Flutter Web on Firebase Hosting.
   While this integration is maintained by Googlers it is not a supported Firebase product.
   Issues filed on GitHub will be addressed on a best-effort basis by maintainers and other community members.

   Documentation: https://firebase.google.com/docs/hosting/frameworks/frameworks-overview
   File a bug: https://github.com/firebase/firebase-tools/issues/new?template=bug_report.md
   Submit a feature request: https://github.com/firebase/firebase-tools/issues/new?template=feature_request.md

   We'd love to learn from you. Express your interest in helping us shape the future of Firebase Hosting: https://goo.gle/41enW5X


Compiling lib/main.dart for the Web...                             804ms
✓ Built build/web

=== Deploying to 'PROJECT_ID'...

i  deploying hosting
i  hosting[aalej-test-site]: beginning deploy...
i  hosting[aalej-test-site]: found 30 files in .firebase/aalej-test-site/hosting
✔  hosting[aalej-test-site]: file upload complete
i  hosting[aalej-test-site]: finalizing version...
✔  hosting[aalej-test-site]: version finalized
i  hosting[aalej-test-site]: releasing new version...
✔  hosting[aalej-test-site]: release complete

✔  Deploy complete!
```
