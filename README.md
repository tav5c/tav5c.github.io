## Features

- **Dynamic Hover Effects** - Mouse-tracking radial gradient that follows cursor movement across interactive elements
- **Particle System** - Interactive particles with connection lines and trailing effects
- **Discord Integration** - Live presence display via Lanyard API showing current activity and status
- **GitHub Showcase** - Automatically fetches and displays latest repositories with stars, forks, and metadata
- **Music Player** - Integrated audio player with vertical volume control and album artwork
- **Donation Section** - Cryptocurrency wallet addresses with smooth copy-to-clipboard functionality
- **Frosted Glass Effects** - Modern glassmorphism design with backdrop blur effects
- **Responsive Design** - Optimized for both desktop and mobile devices with adaptive layouts
- **Custom Animations** - Smooth transitions, hover effects, scroll animations, and glitch effects
- **Background Video** - Looping video background with fallback image support

## Live Demo

Visit: [https://tav5c.github.io](https://tav5c.github.io)

## Quick Start

1. Fork or download this repository
2. Edit the following in `index.html`:

### Personal Information

```javascript
//  - GitHub username
const username = 'your-github-username';

// - Discord user ID (for Lanyard API)
const res = await fetch('https://api.lanyard.rest/v1/users/YOUR_DISCORD_ID');

// - Discord avatar ID
const avatarUrl = `https://cdn.discordapp.com/avatars/YOUR_DISCORD_ID/${avatarHash}.${extension}`;

// - Contact links
const contacts = [
    { name: 'DISCORD', icon: '...', url: 'your-discord-link' },
    { name: 'STEAM', icon: '...', url: 'your-steam-link' },
    { name: 'INSTAGRAM', icon: '...', url: 'your-instagram-link' },
    { name: 'GITHUB', icon: '...', url: 'your-github-link' }
];
```

### Media Files

Replace these with your own assets:

```html
<!-- Background video -->
<source src="assets/bg.mp4" type="video/mp4">
<source src="assets/bg.webm" type="video/webm">

<!-- Background music -->
globalAudio = new Audio('assets/audio.mp3');

<!-- Music metadata -->
songNameEl.textContent = "Your Song Name - Artist (version)";
const songCoverUrl = 'your-album-cover-url';
const songPageUrl = 'your-song-link-url';
const songPageLabel = 'Spotify'; // or 'YouTube', 'SoundCloud', etc.
```

### Custom Font

```css
/* - Font face */
@font-face {
    font-family: 'Chomsky';
    src: url('assets/font.otf') format('opentype');
}
```

3. Place your assets in the `assets/` folder:
   - `bg.mp4` - Background video
   - `font.otf` - Custom font file
   - `audio.mp3` - Background music

4. Deploy to GitHub Pages or any static hosting service

## Customization

### Color Scheme

Edit CSS variables at the top of the `<style>` section:

```css
:root {
    --primary-red: #DC143C;
    --dark-red: #8B0000;
    --light-red: #FF1744;
    --text-shadow-red: rgba(220, 20, 60, 0.5);
    --bg-dark: #000;
    --text-light: #fff;
    --text-gray: #aaa;
    --bg-overlay: rgba(15, 10, 15, 0.185);
    --border-red: rgba(220, 20, 60, 0.4);
    --shadow-red: rgba(220, 20, 60, 0.4);
}
```

### Particle Count

Adjust in the `initParticles()` function:

```javascript
const count = isMobile ? 5 : 40; // Mobile : Desktop
```

### Dynamic Hover Effect

Control the radial gradient intensity:

```css
.dynamic-hover::before {
    background: radial-gradient(
        circle at var(--mouse-x, 50%) var(--mouse-y, 50%), 
        rgba(220, 20, 60, 0.15) 0%,  /* Adjust opacity here */
        transparent 70%                /* Adjust spread here */
    );
}
```

### Donation Button Colors

Customize crypto-specific hover colors:

```css
/* Bitcoin - Orange */
.wallet-option:nth-child(1):hover {
    border-color: #F7931A !important;
}

/* Ethereum - Blue */
.wallet-option:nth-child(2):hover {
    border-color: #627EEA !important;
}

/* Litecoin - Silver Blue */
.wallet-option:nth-child(3):hover {
    border-color: #345D9D !important;
}

/* Monero - Orange */
.wallet-option:nth-child(4):hover {
    border-color: #FF6600 !important;
}
```

## File Structure

```
portfolio/
├── index.html          # Main HTML file with embedded CSS and JavaScript
├── assets/
│   ├── bg.mp4         # Background video
│   ├── font.otf       # Custom font
│   └── audio.mp3      # Background music
└── README.md          # This file
```

## File Hosting Options

This portfolio uses external hosting for media files:

- **GitHub Releases** - Free, reliable for project assets
- **catbox.moe** - Quick file hosting, no account needed
- **Cloudinary** - CDN with optimization features
- **Self-hosted** - Local assets folder for complete control

## Browser Support

- Chrome, Edge, Brave (Chromium-based browsers)
- Firefox
- Safari
- Mobile browsers (iOS Safari, Chrome Mobile)

**Note:** Requires JavaScript enabled for full functionality

## Performance Optimizations
- Passive event listeners for smooth scrolling
- Throttled scroll events for better performance
- Conditional rendering based on device capabilities
- Lazy loading for resources
- GPU-accelerated transforms and animations

## Interactive Features
### Dynamic Hover System

Elements with the `dynamic-hover` class track mouse position and display a radial gradient that follows the cursor:

- Music player
- Time display
- Discord activity card
- Project cards
- Audio volume slider
- Donation buttons

### Donation Section

- Click to copy wallet addresses
- Smooth state transitions from idle to copied
- Vibrate effect on click
- Heart particle animations on hover
- Color-coded borders matching each cryptocurrency
- Auto-reset after 2 seconds

### Music Player

- Play/pause controls
- Vertical volume slider
- Album artwork with hover popup
- Link to song on streaming platform
- Animated music note particles
- Mobile-friendly controls

## APIs Used

- **GitHub API** - Repository data and statistics
- **Lanyard API** - Real-time Discord presence
- **Simple Icons CDN** - Social media and cryptocurrency icons

## Animation Details

### Glitch Effect
Triggered on donation button clicks for visual feedback

### Heart Particles
Float upward on hover over donation elements

### Flame Border
Animated border glow on interactive elements

### Scroll Parallax
Background grid and shapes move at different speeds

### Fade-in Animations
Project cards and sections appear on scroll into view

## Known Limitations

- Particle system disabled on mobile for performance
- Background video may not autoplay on some iOS devices
- Custom cursor hidden on touch devices
- Some animations reduced on mobile browsers
- Clipboard API requires HTTPS for deployment

## Troubleshooting

### Video not playing
- Check video format compatibility (MP4 H.264 recommended)
- Ensure video file is accessible
- Some browsers block autoplay with sound (use muted attribute)

### Music not playing
- User interaction required before audio can play (browser security)
- Check audio file format (MP3 recommended)
- Verify file path is correct

### Discord status not showing
- Verify Discord user ID is correct
- Ensure Lanyard bot is in a server with your Discord account
- Check browser console for API errors

### Particles not visible
- Check if running on mobile (disabled by default)
- Verify canvas element exists
- Check browser console for JavaScript errors

## License

Free to use for personal portfolios. Please don't copy directly - use it as inspiration and make it your own.

## Credits

- Font: Chomsky (custom)
- Icons: [Simple Icons](https://simpleicons.org/)
- Discord Integration: [Lanyard](https://github.com/Phineas/lanyard)
- Design Inspiration: Modern glassmorphism and brutalist aesthetics

---

**Note:** Remember to replace all placeholder URLs, IDs, and wallet addresses with your own information before deploying.
