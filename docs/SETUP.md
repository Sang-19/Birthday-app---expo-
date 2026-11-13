# Newtown Runners Birthday Tracker — Expo Setup

The full working source is provided in the downloadable project archive attached to this conversation. This guide covers Firebase setup.

## Firebase
1. Create a Firebase project and add a Web app.
2. Enable Authentication → Email/Password.
3. Create the admin account using newtownrunners@gmail.com and verify the email address.
4. Create Cloud Firestore.
5. Publish the rules from firestore.rules.
6. Copy .env.example to .env and fill the Firebase public app config.

## Run
npm install
npx expo start

Press a to launch Android, or scan the QR code using Expo Go.
To run the web target, use npm run web.

## Android APK
npm install -g eas-cli
eas login
eas build:configure
eas build --platform android --profile preview

The Firestore rules are the enforcement point: reads are public, writes require an authenticated and verified newtownrunners@gmail.com account.