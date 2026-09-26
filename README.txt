DATABASE — WEB APP v2

WHAT CHANGED
- App name changed from Surat Business Book to DATABASE.
- Location is now generic. You can record Surat, Ahmedabad, Tiruppur, Erode, Jodhpur, or any place.
- Online/cloud-ready with Firebase Authentication, Firestore and Cloud Storage.
- Each signed-in user gets a private database path.
- Photos and videos upload to Firebase Storage and are linked to the record.
- Multiple fabric qualities can be stored in one Fabric record.
- Backup export/import is included.

FIRST TIME SETUP
1. Open Firebase Console and create a project.
2. Add a Web App to the Firebase project.
3. Enable Authentication → Google.
4. Create Cloud Firestore Database.
5. Enable Storage.
6. Open firebase-config.js and paste the Web App config values.
7. In Firebase Console, add your local development domain / hosting domain to Authentication → Settings → Authorized domains if needed.
8. Keep firestore.rules and storage.rules as provided.
9. Test locally with VS Code Live Server.
10. Deploy to Firebase Hosting using the commands below.

FIREBASE HOSTING
Install/update Firebase CLI:
  npm install -g firebase-tools

Login:
  firebase login

From this folder:
  firebase init hosting firestore storage

Select the Firebase project. For the hosting public directory, enter . and keep the single-page app rewrite.

Deploy:
  firebase deploy

The app will be available on the Firebase-provisioned web.app domain.

IMPORTANT
- Do not share your Firebase config file together with private admin credentials. The Web App config itself is intended for client apps; your real protection comes from Authentication + Firestore/Storage Security Rules.
- This version is built for your personal / small-team database first. Later we can add roles, team sharing, advanced search, reminders, maps, supplier/buyer history, OCR, duplicate detection, and better mobile/PWA support.
