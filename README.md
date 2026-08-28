# 🎂 Interactive Birthday Surprise Website ✨

A delightful, magical, and fully responsive interactive birthday surprise web application crafted with React, Vite, Framer Motion, and Node/Express.

---

## 🚀 Quick Start Guide

### 1. Run Everything (Frontend + Backend)
In your terminal, navigate to the project directory and run:
```bash
npm run dev
```
- 🌐 **Birthday Experience:** [http://localhost:5173](http://localhost:5173)
- ⚙️ **Admin Dashboard:** [http://localhost:5173/admin](http://localhost:5173/admin)
- 🔌 **Backend API:** [http://localhost:5000/api/birthday](http://localhost:5000/api/birthday)

---

## 🎨 How to Personalize Your Website

Everything is beginner-friendly and designed so you don't have to touch complex React code.

### 1. 🖼️ Where to Put Your Photos
Put your images in:
```
public/assets/photos/
```
For example, save your photos as:
- `photo1.jpg` (or `.png` / `.webp`)
- `photo2.jpg`
- `photo3.jpg`
- `photo4.jpg`
- `photo5.jpg`
- `photo6.jpg`

Then in `src/config/birthdayConfig.js`, update the `url` to point to `/assets/photos/photo1.jpg`.

---

### 2. 📝 Where to Edit Birthday Text, Recipient Name & PIN
Open the file:
```
src/config/birthdayConfig.js
```
*(and optionally `server/data/birthday.json`)*

You can edit:
- **Recipient's Name:** Change `recipientName: "NAME_HERE"` to your loved one's name (e.g. `recipientName: "Sarah"`).
- **Secret Unlock PIN:** Change `pin: "1234"` to any 4-digit code (e.g. `pin: "0828"` or their birthday).
- **Birthday Messages:** Customize headings, surprise questions, and the final handwritten letter lines.
- **Gift Messages & Vouchers:** Customize the title, message revealed, and surprise tags for each gift box.

---

### 3. ⚙️ Using the Visual Admin Panel
If you prefer a visual interface without opening code files:
1. Open [http://localhost:5173/admin](http://localhost:5173/admin) in your browser.
2. Edit names, PIN, messages, or upload photos directly from your computer.
3. Click **"Save All Changes"**. All changes will update immediately!

---

### 4. 🎶 Adding Background Music
Place your favorite song or birthday track in:
```
public/assets/music/birthday.mp3
```
*Note: If no audio file is added, the website includes a built-in music-box lullaby synthesizer, so audio works smoothly out of the box!*

---

## 📱 Interactive Website Flow

1. 🔒 **Screen 1 — Unlock Screen:** Enter the secret PIN with a playful keypad and cute photo frame. Wrong PIN gives a gentle shake; correct PIN triggers a sparkle unlock.
2. 💌 **Screen 2 — Surprise Question:** "I have little surprise for you. Wanna see it?" with a lively YES button and a playful dodging NO button!
3. 🎂 **Screen 3 — Birthday Celebration:** "HAPPY BIRTHDAY [NAME]" with colorful banners, floating balloons, photo frame, and falling confetti.
4. 📸 **Screen 4 — Memory Gallery:** Smooth carousel displaying photos, dates, sweet captions, and memory notes.
5. 🎁 **Screen 5 & 6 — Gift Selection & Reveal:** Interactive gift boxes that wobble and pop open with confetti, revealing personalized surprises and vouchers.
6. 💖 **Screen 7 — Final Heartfelt Message:** Emotional handwritten card with floating hearts, photo, and a **"Replay Surprise 🔄"** button.

---

## 🛠️ Project Structure

```
birthday/
├── public/
│   └── assets/
│       ├── photos/           # 📸 Put your photos here
│       ├── gifts/            # 🎁 Put your custom gift icons here
│       ├── decorations/      # 🎈 SVG balloons, cakes, banners
│       └── music/            # 🎵 Put birthday.mp3 here
├── src/
│   ├── config/
│   │   └── birthdayConfig.js # 📝 Master editable configuration file
│   ├── components/
│   │   ├── UnlockScreen.jsx  # Screen 1: Keypad & PIN lock
│   │   ├── SurpriseScreen.jsx# Screen 2: YES / dodging NO question
│   │   ├── BirthdayScreen.jsx# Screen 3: Happy Birthday celebration
│   │   ├── MemoryGallery.jsx # Screen 4: Memory photo carousel
│   │   ├── GiftSelection.jsx # Screen 5 & 6: Gift unboxing & reveal
│   │   ├── FinalMessage.jsx  # Screen 7: Emotional letter & replay
│   │   ├── Layout.jsx        # Mobile-first responsive wrapper
│   │   ├── MusicControl.jsx  # Floating music player toggle
│   │   ├── FloatingBalloons.jsx # Ambient pastel balloons & sparkles
│   │   └── ConfettiCanvas.jsx# Festive confetti explosion engine
│   ├── pages/
│   │   ├── Home.jsx          # Main surprise sequence orchestrator
│   │   └── Admin.jsx         # /admin visual customization dashboard
│   ├── services/
│   │   └── birthdayApi.js    # API service client
│   └── index.css             # Soft pastel theme & animations
├── server/
│   ├── server.js             # Express API backend & file upload handler
│   └── data/
│       └── birthday.json     # Persistent data store
└── package.json
```
