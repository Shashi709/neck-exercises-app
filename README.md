# Neck Exercises Guide App

A simple, responsive, and user-friendly web app for physiotherapy neck exercises.  
This app helps you perform, track, and time common neck warm-up and strengthening exercises — with clear instructions and a customizable timer for each.

---

## 🚀 Features

- **Warm-up and strengthening exercises** (with emoji icons)
- **Customizable reps and hold time** for each exercise
- **Start / Pause / Resume / Reset** per exercise
- **Loud beep sound** for guidance and completion
- **Dark mode support** with theme persistence
- **Admin panel sequencer** - Run all exercises automatically with 10s delays
- **Fully responsive** - Works perfectly on mobile, tablet & desktop
- **Offline support** - Works without internet after first load (PWA)
- **No install required** - Runs directly in browser

---

## 📋 Usage

### Main App (index.html)
1. **Open the app** - Just click `index.html` or visit the live link
2. **For each exercise:**
   - Read the instructions
   - Set number of reps & seconds per rep (default values provided)
   - Click **Start**
   - Follow the beep and timer for every repetition
   - Use **Pause/Resume/Reset** as needed
3. **Toggle dark mode** - Click 🌙 button (top-right)
4. **Go to Admin** - Click ⚙️ button to access sequencer

### Admin Panel (admin.html)
- **Select All / Deselect All** - Choose which exercises to run
- **Start All** - Begin automatic sequencer (exercises run one-by-one)
- **Pause All / Resume All** - Control execution
- **Reset All** - Clear all exercises
- **10-second delay** between exercises for rest periods
- Same dark mode & back navigation as main app

---

## 🛠️ Installation & Setup

### Local Development
```bash
# Clone the repository
git clone https://github.com/Shashi709/neck-exercises-app.git
cd neck-exercises-app

# Open in browser
# Just open index.html in your browser - no build steps needed!
```

### Live Demo
Visit: https://shashi709.github.io/neck-exercises-app/

---

## 📁 Project Structure

```
neck-exercises-app/
├── index.html              # Main exercises page
├── admin.html              # Admin sequencer panel
├── service-worker.js       # Offline caching (PWA)
├── manifest.json           # PWA configuration
├── README.md              # Documentation
└── .git/                  # Git repository
```

---

## 💾 Technical Details

### Technologies Used
- **HTML5** - Semantic markup
- **CSS3** - Responsive design with 5 media breakpoints
- **Vanilla JavaScript** - No dependencies
- **Web Audio API** - Sound generation
- **Service Worker** - Offline caching
- **LocalStorage** - Theme persistence

### Responsive Breakpoints
- 900px (tablets)
- 650px (large phones)
- 480px (standard phones)
- 360px (small phones)

### Features
- **Dark Mode** - Toggle with 🌙 button, saved in localStorage
- **Offline Support** - Works completely offline after first visit
- **PWA Ready** - Add to home screen on mobile devices
- **Sequencer** - Auto-run exercises with customizable delays

---

## 📝 Exercise Defaults

### Warm-up
- **Neck Rotation** - 20 reps × 12 sec
- **Neck Side Bending** - 20 reps × 12 sec

### Strengthening
- **Front + Back Neck Isometric** - 20 reps × 12 sec
- **Side Neck Isometric** - 20 reps × 12 sec
- **Shoulder Shrugs** - 20 reps × 12 sec
- **Arm Swinging** - 8 reps × 10 sec

---

## ⚠️ Important Safety Notes

**If you experience any pain, STOP exercising immediately!**

This app is designed as a guide. Please consult a healthcare professional before starting any new exercise program.

---

## 🔄 Offline & Mobile Features

### PWA Installation
1. Open app on mobile browser
2. Tap menu → "Add to Home Screen" (Android) or "Share" → "Add to Home Screen" (iOS)
3. App appears on home screen
4. Tap to launch as standalone app

### Offline Usage
- App caches on first visit
- Works 100% offline after that
- All data persists in localStorage
- Automatically syncs when back online

---

## 🎨 Customization

### Change Exercise Defaults
Edit `defaultReps` and `defaultSeconds` in the `exerciseSections` array in `index.html`:

```javascript
{
  name: "Your Exercise",
  icon: "🏋️",
  description: "Exercise description here",
  defaultReps: 15,
  defaultSeconds: 10
}
```

### Theme Colors
Update CSS variables in the `<style>` section:
- Primary: `#2563eb`
- Dark mode: `#07101a`
- Accent colors for buttons (pause, resume, reset)

---

## 📱 Browser Support

- Chrome/Edge 80+
- Firefox 75+
- Safari 13+
- Mobile browsers (iOS Safari, Chrome Mobile)

---

## 📄 License

Open source - Feel free to use, modify, and share!

---

## 👤 Author

Created by **Shashi Raj**  
GitHub: [@Shashi709](https://github.com/Shashi709)

---

## 🆘 Troubleshooting

### Sounds not playing?
- Ensure browser audio is not muted
- Click anywhere on the app first (browser security requirement)
- Check browser console (F12) for errors

### Dark mode not persisting?
- Check if localStorage is enabled in browser
- Try clearing browser cache and reloading

### Offline not working?
- Open app once to register Service Worker
- Check browser DevTools → Application → Service Workers
- Ensure you're using HTTPS (or localhost for testing)

---

## 🚀 Future Enhancements

- [ ] Sound customization options
- [ ] Exercise history tracking
- [ ] Progress statistics
- [ ] Custom exercise creation
- [ ] Workout presets
- [ ] Mobile app (React Native)

---
