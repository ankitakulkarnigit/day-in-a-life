# Day in a Life 🔥

A personal daily habit tracker with streaks, XP, achievements, and Instagram sharing. Syncs across devices via Firebase.

## Setup

### 1. Clone the repo
```bash
git clone https://github.com/ankitakulkarnigit/day-in-a-life.git
cd day-in-a-life
```

### 2. Configure your Firebase API key

**a. Create a Firebase project**
1. Go to [console.firebase.google.com](https://console.firebase.google.com)
2. Click **Add project** → name it → follow the steps

**b. Enable Google Sign-In**
1. Build → **Authentication** → Get started
2. Sign-in method → **Google** → Enable → add your email as support email → Save

**c. Create Firestore database**
1. Build → **Firestore Database** → Create database
2. Select **Start in test mode** → choose a region → Done

**d. Get your config**
1. Click the ⚙️ gear icon → **Project settings**
2. Scroll to **Your apps** → click `</>` (Web) → register the app
3. Copy the `firebaseConfig` object

**e. Add config to the project**
```bash
cp firebase-config.example.js firebase-config.js
```
Open `firebase-config.js` and paste in your values:
```js
const FIREBASE_CONFIG = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.firebasestorage.app",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```

> 🔒 `firebase-config.js` is gitignored and will never be committed.

### 3. Run locally
```bash
python3 -m http.server 8080
```
Then open **http://localhost:8080** in your browser.

> ⚠️ Do not open `index.html` directly as a file — Firebase Auth requires `http://` to work.

### 3. App hosted at

https://ankitakulkarnigit.github.io/day-in-a-life/

## Daily Goals
1. 🥑 Fat First Morning
2. 🥚 Protein Rich Breakfast
3. 👟 2K Steps
4. 📚 Learning
5. 🥗 Protein & Fiber Lunch
6. 🚶 3K Steps
7. 🍎 Mindful Snack / Pre-workout
8. 💪 Gym / 8K Steps
9. 🌙 Low Carb Dinner
10. 🧠 Reading/Learning

## Features
- 🔥 Streak tracking with XP & level system
- 📊 Activity heatmap, charts & achievements
- 📸 Instagram share card generator
- ☁️ Cross-device sync via Firebase Firestore
- 🔐 Google Sign-In authentication
