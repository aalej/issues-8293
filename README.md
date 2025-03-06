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

```
$ firebase deploy --project PROJECT_ID

   Thank you for trying our experimental support for Flutter Web on Firebase Hosting.
   While this integration is maintained by Googlers it is not a supported Firebase product.
   Issues filed on GitHub will be addressed on a best-effort basis by maintainers and other community members.

   Documentation: https://firebase.google.com/docs/hosting/frameworks/frameworks-overview
   File a bug: https://github.com/firebase/firebase-tools/issues/new?template=bug_report.md
   Submit a feature request: https://github.com/firebase/firebase-tools/issues/new?template=feature_request.md

   We'd love to learn from you. Express your interest in helping us shape the future of Firebase Hosting: https://goo.gle/41enW5X


Compiling lib/main.dart for the Web...                             674ms
✓ Built build/web

=== Deploying to 'PROJECT_ID'...

i  deploying hosting
i  hosting[PROJECT_ID]: beginning deploy...
i  hosting[PROJECT_ID]: found 30 files in .firebase/PROJECT_ID/hosting
✔  hosting[PROJECT_ID]: file upload complete
i  hosting[PROJECT_ID]: finalizing version...
✔  hosting[PROJECT_ID]: version finalized
i  hosting[PROJECT_ID]: releasing new version...
✔  hosting[PROJECT_ID]: release complete

✔  Deploy complete!
```
