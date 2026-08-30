# Lot-picker
final end winner

## WhatsApp-style phone sign-in setup

This app uses Firebase Authentication phone OTP for WhatsApp-style login and Firestore for protected user activity and feedback records.

1. Create a Firebase project.
2. Enable Authentication > Sign-in method > Phone.
3. Add `rakir4898-dev.github.io` to Authentication > Settings > Authorized domains.
4. Enable Firestore Database.
5. Copy `firebase-config.sample.json` to `firebase-config.json` and fill in the Firebase web app config.
6. Deploy the Firestore rules from `firestore.rules`.
7. Commit and push `firebase-config.json` so GitHub Pages can load it.

`firebase-config.json` is public browser configuration. Access control for login history, app activity, and feedback must be enforced by Firestore security rules, not by hiding client-side files. WhatsApp group membership cannot be verified directly by WhatsApp; the app treats the approved phone-number roster as the WhatsApp group access list.
