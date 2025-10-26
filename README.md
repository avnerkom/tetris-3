# 🎮 Advanced 3D Tetris Game

A feature-rich, modern implementation of Tetris with stunning 3D graphics, dynamic audio, and an impressive array of gameplay enhancements. Built with vanilla JavaScript, Three.js, and Tone.js.

![Tetris Game](https://img.shields.io/badge/Status-Production-brightgreen) ![License](https://img.shields.io/badge/License-MIT-blue)

## 🌟 Live Demo

[Play the game here!](#) *(Add your GitHub Pages link)*

---

## 💭 Project Background

This project is a heartfelt tribute to **The New Tetris** from the Nintendo 64—a game I absolutely loved many years ago. My goal was to recreate the essence of that classic experience and bring it to the modern web, making it accessible to everyone, anywhere, on any device.

### Inspiration & Vision

Using modern web technologies like **Three.js** and **Tone.js**, I've rebuilt the core features that made The New Tetris so memorable:
- ✅ **3D graphics and camera rotation** for that immersive N64 feel
- ✅ **Hold system** to strategically save pieces
- ✅ **Enhanced scoring** with massive multi-line bonuses
- ✅ **Progressive difficulty** with level-based multipliers
- ✅ **Dynamic audio** that adapts to gameplay
- ✅ **Epic celebrations** for high scores and records

### What's Missing (For Now)

While this version captures all the essential gameplay mechanics, some visual flourishes from the original aren't yet implemented:
- The beautiful "skating" animations of new pieces entering from the right side
- Dynamic changing backgrounds as you progress through levels
- Some of the original's visual polish and particle effects

But fear not—**all the core features that made the game addictive are here!** The spirit of The New Tetris lives on in this accessible, browser-based version that anyone can play without needing an N64 console.

---

## ✨ Features Overview

This isn't your average Tetris clone! This implementation includes **40+ advanced features** that create an unforgettable gaming experience.

---

## 🎨 Graphics & Rendering

### Dual Rendering Modes
- **3D Mode**: Stunning WebGL-powered 3D graphics using Three.js
  - Realistic depth and perspective
  - Smooth camera transitions
  - Interactive camera rotation (mouse drag/touch swipe)
  - Dynamic lighting and shadows
- **2D Mode**: Classic pixel-perfect 2D rendering
  - Canvas-based graphics
  - Retro aesthetic
  - Optimized performance
- **Seamless Toggle**: Switch between 2D and 3D anytime during gameplay!

### Visual Effects
- **Floating Score Animations**: See your points fly up when clearing multiple lines!
- **Fireworks Display**: Spectacular particle effects for high scores
- **Epic #1 Record Celebration**:
  - Screen shake effect
  - 3× fireworks intensity
  - Golden confetti rain (50 particles)
  - Pulsing 👑 NEW #1 RECORD badge
- **Level-Up Notifications**: Animated badges with score multiplier info
- **Neon Arcade Aesthetic**: Glowing borders, gradients, and cyberpunk vibes

---

## 🎵 Dynamic Audio System

### Music Engine (Powered by Tone.js)
- **Procedurally Generated Music**: Real-time synthesis, no audio files!
- **Adaptive Tempo**: Music speeds up as you level up
  - Base tempo: 140 BPM
  - Increases by 15% per level
- **Multi-Track Composition**:
  - Lead melody (alternating A/B patterns)
  - Bass line
  - Hi-hat rhythm
  - Kick drum
  - Snare drum

### Sound Effects
- **Lock**: When piece lands
- **Clear**: Line clear sound
- **Tetris**: Special sound for 4-line clears
- **Rotate**: Piece rotation feedback
- **Game Over**: End game sound
- **Mute/Unmute Toggle**: Desktop and mobile controls

---

## 🎯 Advanced Scoring System

### Multi-Line Bonuses
Gone are the boring linear scores! This game rewards skillful play:

| Lines Cleared | Base Score Formula | With Level Multiplier |
|--------------|-------------------|----------------------|
| Single (1)   | 100 × level       | Standard             |
| **DOUBLE (2)** | 400 × level       | +300% bonus + floating text! |
| **TRIPLE (3)** | 800 × level       | +700% bonus + floating text! |
| **TETRIS (4)** | 1,600 × level     | +1,500% bonus + floating text! |

### Level-Based Score Multipliers
Starting from **Level 3**, earn progressive multipliers:
- Level 1-2: 1.0× (no bonus)
- Level 3: 1.2× (+20% bonus)
- Level 4: 1.4× (+40% bonus)
- Level 5: 1.6× (+60% bonus)
- Level 6: 1.8× (+80% bonus)
- Level 7+: 2.0× and beyond! (+100%+)

**Example**: A Tetris at Level 5 = 1,600 × 5 × 1.6 = **12,800 points!** 🔥

### Real-Time Feedback
- **Floating Score Text**: Displays "DOUBLE! +XXX", "TRIPLE! +XXX", or "TETRIS! +XXX"
- **Golden glow effect** with upward animation
- Auto-fades after 2 seconds

---

## 🏆 High Scores & Leaderboard

### Top 10 Leaderboard
- **Dual Storage System**:
  - Local storage (always available)
  - Firebase Firestore (cloud sync when configured)
- **Special Styling for Top 3**:
  - 🥇 **1st Place**: Gold gradient, large text, glowing border
  - 🥈 **2nd Place**: Silver gradient, medium text
  - 🥉 **3rd Place**: Bronze gradient, bold text

### Smart Name Management
- **Auto-save**: Your name is remembered across sessions
- **8 Character Limit**: Prevents scoreboard overflow
- **Ellipsis Overflow**: Long names get "..." treatment
- **Flexible Layout**: Scoreboard adapts to any name length

### Celebration System
- **Top 10 Score**: Fireworks display (8 bursts)
- **New #1 Record**:
  - Entire screen shakes
  - 24 fireworks (3× normal)
  - 50 golden confetti pieces
  - Pulsing crown badge for 5 seconds

---

## 🎮 Enhanced Gameplay Features

### Hold System
- Press **C** (or tap Hold button) to save current piece
- Swap with held piece anytime
- One swap per piece drop
- Visual preview of held piece

### Level Progression
- **10 lines per level**
- **Progressive difficulty**: Speed increases with each level
- **Level-up pause**: Game pauses for 2.5 seconds to display achievement
  - Shows new level number
  - Displays score multiplier (from level 3+)
  - Music continues playing!
- **Real-time tracker**: "X more lines to level Y" display

### Game Over Options
Three strategic choices when you lose:
1. **Play Again**: Fresh start at Level 1
2. **Start at Level X**: Practice higher difficulty (score resets to 0)
3. **Quit to Main Screen**: Return to start

---

## 🎛️ Controls

### Desktop (Keyboard)
| Action | Key(s) |
|--------|--------|
| Move Left | ← Arrow |
| Move Right | → Arrow |
| Soft Drop | ↓ Arrow |
| Hard Drop | Spacebar |
| Rotate | ↑ Arrow |
| Hold/Swap | C |
| Pause/Resume | P or ESC |
| Rotate Camera (3D) | Mouse Drag |
| Resume from Pause | Click game board or pause text |
| Help | ? |

### Mobile (Touch)
- **On-screen buttons**: Movement, rotation, drop, hold
- **Swipe gesture**: Drag on game board to rotate 3D camera
- **Tap to resume**: Tap "GAME PAUSED" or game board when paused

---

## 💡 UX Enhancements

### Pause System
- **Visual overlay**: Large blinking "GAME PAUSED" text with hint
- **Click-to-resume**: Click anywhere on game board or pause text
- **Hover effect**: Pause text scales on hover
- **Music continues**: Only gameplay pauses, music keeps playing

### Smart Input Handling
- **Prevents page scrolling**: Arrow keys won't scroll the page during gameplay
- **No autocomplete interference**: Disabled browser autocomplete/autocorrect
- **Input field detection**: Game controls disabled when typing
- **Can't type 'C' issue**: Fixed! Works in all input fields

### Level-Up Experience
- **Auto-pause**: Game freezes while showing level-up notification
- **Music continues**: Audio keeps playing for smooth experience
- **Controls disabled**: No accidental moves during celebration
- **Auto-resume**: Returns to gameplay after 2.5 seconds

### Quality of Life
- **Name persistence**: Enter once, saved forever
- **Lines to next level**: Always know how close you are
- **Mode memory**: Remembers 2D/3D preference
- **Console clean**: No annoying warnings or logs
- **Responsive design**: Perfect on desktop, tablet, and mobile

---

## 🏗️ Technical Architecture

### Clean Code Principles
- **Modular design**: 14 logical modules
  - Utils
  - Piece Management
  - Board Logic
  - Game Loop
  - 3D Rendering
  - 2D Rendering
  - Audio System
  - Storage Management
  - Visual Effects
  - UI Management
  - Input Handling
- **SOLID principles**: Single responsibility, dependency injection
- **DRY code**: No duplication, reusable functions
- **Small functions**: Average 5-15 lines per function
- **DOM caching**: All elements cached, no repeated queries
- **Magic numbers eliminated**: All values in CONFIG object

### Technologies Used
- **JavaScript (ES6+)**: Modern vanilla JS, no frameworks
- **Three.js**: WebGL 3D rendering
- **Tone.js**: Web Audio API synthesis
- **Firebase**: Cloud storage (optional)
- **Tailwind CSS**: Utility-first styling
- **HTML5 Canvas**: 2D rendering fallback

### Performance Optimizations
- **RequestAnimationFrame**: Smooth 60 FPS gameplay
- **Efficient rendering**: Only updates what changed
- **Memory management**: Automatic cleanup of particles and effects
- **Lazy initialization**: Audio/Firebase loaded on demand

---

## 📦 File Structure

```
tetris/
├── Tetris_final.html       # Main game file (single-file architecture)
├── README.md               # This file
└── screenshots/            # (Optional) Game screenshots
```

**Single File Design**: Everything in one HTML file for easy deployment!

---

## 🚀 Getting Started

### Quick Start (No Installation!)
1. Download `Tetris_final.html`
2. Open in any modern web browser
3. Click "START GAME" and enjoy!

### Firebase Setup (Optional)
To enable cloud high scores:

1. Create a Firebase project at [firebase.google.com](https://firebase.google.com)
2. Enable Firestore Database
3. Add your config to the file:

```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    // ... other config
};
```

4. Set Firestore rules:
```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /artifacts/{appId}/public/data/tetris_3d_high_scores/{document=**} {
      allow read: if true;
      allow write: if request.auth != null;
    }
  }
}
```

**Note**: Game works perfectly without Firebase using localStorage!

---

## 🎨 Customization

### Scoring Formulas
Adjust in `Board.updateScore()`:
```javascript
if (linesCleared === 4) {
    baseScore = 1600 * state.level; // Change this!
}
```

### Level Speed
Modify in `CONFIG`:
```javascript
const CONFIG = {
    INITIAL_DROP_INTERVAL: 1000,  // Starting speed (ms)
    LEVEL_SPEED_MULTIPLIER: 0.15, // Speed increase per level
    LINES_PER_LEVEL: 10,          // Lines needed to level up
    // ...
};
```

### Colors
Change piece colors in `COLORS` object:
```javascript
const COLORS = {
    1: '#FF0D72', // T-piece
    2: '#0DC2FF', // I-piece
    // ... customize away!
};
```

---

## 🐛 Known Issues & Solutions

### Audio Not Playing?
- **Solution**: Click anywhere on the page first (browser autoplay policy)

### Slow Performance on Mobile?
- **Solution**: Switch to 2D mode for better performance

### Scores Not Saving to Cloud?
- **Solution**: Check Firebase configuration and authentication

---

## 📝 Version History

### v2.0 - The Ultimate Edition (Current)
- ✨ Added 3D rendering mode with Three.js
- 🎵 Implemented dynamic music system
- 🏆 Enhanced scoring with multi-line bonuses
- 🎯 Level-based score multipliers
- 🎆 Epic celebration effects
- 💾 Dual storage system
- 📱 Full mobile support
- 🎮 Click-to-resume feature
- 🔄 Start at same level option
- 📊 Top 10 leaderboard with special top 3 styling
- And 30+ more features!

### v1.0 - Classic Implementation
- Basic Tetris gameplay
- 2D canvas rendering
- Simple scoring system

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - feel free to use it in your own projects!

---

## 🙏 Acknowledgments

- **Three.js** - Amazing 3D graphics library
- **Tone.js** - Powerful Web Audio framework
- **Tailwind CSS** - Beautiful utility-first CSS
- **Firebase** - Cloud storage solution
- **The Tetris Company** - For creating the timeless classic

---

## 🎯 Future Enhancements

Ideas for future versions:
- [ ] Multiplayer mode
- [ ] Custom skins/themes
- [ ] Achievement system
- [ ] Replay system
- [ ] Tournament mode
- [ ] Social sharing
- [ ] Mobile app version
- [ ] VR mode support

---

## 💬 Contact

Have questions or suggestions? Feel free to reach out!

- **GitHub**: [Your GitHub Profile](#)
- **Email**: avner.komarow@gmail.com

---

## ⭐ Show Your Support

If you enjoyed this game, please consider:
- Giving it a ⭐ on GitHub
- Sharing it with friends
- Contributing improvements
- Reporting bugs

---

<div align="center">

**Made with ❤️ and lots of ☕**

*Happy Gaming! 🎮*

</div>
