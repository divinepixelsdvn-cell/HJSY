# 🚩 హనుమాన్ శోభాయాత్ర 2026

పెద్దాపురం - సామర్లకోట | మే 12, 2026

---

## 🌐 GitHub Pages మీద Publish చేయడం

### Step 1: GitHub Repository తయారు చేయండి

1. [github.com](https://github.com) లో Login అవ్వండి
2. **New Repository** నొక్కండి
3. Repository name: `hjsy2026` అని పెట్టండి
4. **Public** select చేయండి
5. **Create repository** నొక్కండి

### Step 2: Files Upload చేయండి

1. Repository తెరిచాక **"uploading an existing file"** నొక్కండి
2. `index.html` ని drag & drop చేయండి
3. **Commit changes** నొక్కండి

### Step 3: GitHub Pages Enable చేయండి

1. Repository లో **Settings** → **Pages** కి వెళ్ళండి
2. Source: **Deploy from a branch** select చేయండి
3. Branch: **main** → **/ (root)** select చేయండి
4. **Save** నొక్కండి
5. కొన్ని నిమిషాల్లో site live అవుతుంది:
   `https://YOUR_USERNAME.github.io/hjsy2026/`

---

## 🔥 Firebase Real-Time Sync Setup

అందరి posts అందరికి కనిపించాలంటే Firebase అవసరం.

### Step 1: Firebase Project తయారు చేయండి

1. [console.firebase.google.com](https://console.firebase.google.com) తెరవండి
2. **Add project** → Project name: `hjsy2026` → **Continue**
3. Google Analytics: Disable చేసి **Create project**

### Step 2: Realtime Database Enable చేయండి

1. Left menu లో **Build** → **Realtime Database**
2. **Create Database** నొక్కండి
3. Location: **us-central1** → **Next**
4. **Start in test mode** select చేయండి → **Enable**

### Step 3: Database Rules Update చేయండి

Rules tab లో ఈ rules పెట్టండి (ఎవరైనా చదవగలరు, admin మాత్రమే రాయగలరు):

```json
{
  "rules": {
    "posts": {
      ".read": true,
      ".write": true
    }
  }
}
```

**Publish** నొక్కండి.

### Step 4: Firebase Config తీసుకోండి

1. Firebase Console లో **Project Settings** (⚙️ icon) నొక్కండి
2. **Your apps** section లో **</>** (Web) నొక్కండి
3. App name: `hjsy2026-web` → **Register app**
4. `firebaseConfig` object copy చేయండి

### Step 5: index.html లో Config పెట్టండి

`index.html` లో ఈ భాగం వెతకండి:

```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  ...
};
```

దాని బదులు Firebase నుండి copy చేసిన config పెట్టండి.

### Step 6: Updated index.html ని GitHub లో Upload చేయండి

1. GitHub repository తెరవండి
2. `index.html` నొక్కండి → ✏️ Edit నొక్కండి
3. అన్నీ delete చేసి new content paste చేయండి
4. **Commit changes** నొక్కండి

---

## ✅ Result

- Website: `https://YOUR_USERNAME.github.io/hjsy2026/`
- ఒక్కరు post చేస్తే **అందరికి instant గా కనిపిస్తుంది** 🚀
- Login: ID = `HJSY26`, Password = `051226`

---

## 📱 Features

- 🚩 నమోదు + ID Card download
- 📝 పోస్ట్లు (text + photos + videos)  
- 📸 ఫోటోస్ gallery + download
- 🎬 వీడియోస్
- 📰 న్యూస్
- ❤️ జై శ్రీరామ్ likes
- 🔥 Real-time sync (Firebase)
