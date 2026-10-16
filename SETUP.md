# Turn on shared live data (Firebase, free plan)

1. console.firebase.google.com → Add project (name e.g. sitestock; Analytics off).
2. Build → Firestore Database → Create database → Production mode → pick a nearby region.
3. Firestore → Rules → paste contents of `firestore.rules` → Publish.
4. Build → Authentication → Get started → Sign-in method → enable Email/Password.
   Then Settings → User actions → untick "Enable create (sign-up)" so only people you add can sign in.
5. Authentication → Users → Add user: create an email + password for each staff member.
6. Project settings (gear) → Your apps → Web (</>) → register app → copy the firebaseConfig values.
7. Edit `firebase-config.js` in GitHub (pencil icon) and replace `null` with the config object (see example in file). Commit.
8. Authentication → Settings → Authorized domains → Add `<your-username>.github.io`.
