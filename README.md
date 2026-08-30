# Lot-picker
final end winner

## Authentication setup

This app uses Firebase Authentication for both Google sign-in and WhatsApp-style phone OTP. Users choose the method every time they log in.

1. Create a Firebase project.
2. Enable Authentication > Sign-in method > Google and Phone.
3. Add `rakir4898-dev.github.io` to Authentication > Settings > Authorized domains.
4. Enable Firestore Database.
5. Copy `firebase-config.sample.json` to `firebase-config.json` and fill in the Firebase web app config.
6. Deploy the Firestore rules from `firestore.rules`.
7. Commit and push `firebase-config.json` so GitHub Pages can load it.

`firebase-config.json` is public browser configuration. Access control for login history, app activity, and feedback must be enforced by Firestore security rules, not by hiding client-side files. WhatsApp group membership cannot be verified directly by WhatsApp; the app treats the approved `+91` phone-number roster as the WhatsApp group access list. Google login stores the first Google email used for each roster member and requires the same email on later Google logins.
