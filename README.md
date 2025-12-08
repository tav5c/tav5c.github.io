## Features

- **Particle System** - Interactive particles with connection lines
- **Discord Integration** - Live presence display via Lanyard API
- **GitHub Showcase** - Automatically fetches and displays your latest repositories
- **Music Player** - audio player with volume control
- **Frosted Glass effects** - Modern design with backdrop blur effects
- **Responsive Design** - Optimized for both desktop and mobile devices
- **Custom Animations** - Smooth transitions, hover effects, and scroll animations

## Live Demo

Visit: [https://tav5c.github.io](https://tav5c.github.io)

## Quick Start

1. Fork or download this repository
2. Edit the following in `index.html`:

### Personal Information
```javascript
// Line ~780 - GitHub username
const username = 'your-github-username';

// Line ~863 - Discord user ID (for Lanyard API)
const res = await fetch('https://api.lanyard.rest/v1/users/YOUR_DISCORD_ID');

// Line ~871 - Discord avatar ID
const avatarUrl = `https://cdn.discordapp.com/avatars/YOUR_DISCORD_ID/${avatarHash}.${extension}`;

// Line ~757 - Contact links
const contacts = [
    { name: 'DISCORD', icon: '...', url: 'your-discord-link' },
    { name: 'STEAM', icon: '...', url: 'your-steam-link' },
    { name: 'INSTAGRAM', icon: '...', url: 'your-instagram-link' },
    { name: 'GITHUB', icon: '...', url: 'your-github-link' }
];
```

### Media Files
Replace these URLs with your own:
```html
<!-- Line ~395 - Background video -->
<source src="your-video-url.mp4" type="video/mp4">

<!-- Line ~399 - Fallback background image -->
<img class="bg-fallback" id="bgImage" src="your-image-url.png">

<!-- Line ~701 - Background music -->
globalAudio = new Audio('your-music-url.mp3');

<!-- Line ~710 - Album cover and song name -->
songNameEl.textContent = 'Your Song Name';
albumCover.src = 'your-album-cover-url';
```

### Custom Font (Optional)
```css
/* Line ~43 - Font */
@font-face {
    font-family: 'Chomsky';
    src: url('your-font-url.otf') format('opentype');
}
```

3. Deploy to GitHub Pages or any static hosting

## Customization

### Color Scheme
Edit CSS variables at the top of the `<style>` section (Line ~18):
```css
:root {
    --primary-red: #DC143C;
    --dark-red: #8B0000;
    --light-red: #FF1744;
    /* ... other colors */
}
```

### Particle Count
Adjust in the `initParticles()` function (Line ~572):
```javascript
const count = isMobile ? 10 : 80; // Mobile : Desktop
```

### Volume Range
Change maximum volume (Line ~413):
```html
<input type="range" ... max="300" value="100">
<!-- Max 100 = normal, 200 = 2x, 300 = 3x volume -->
```

## File Hosting

This portfolio uses these hosting for media files. :

- **GitHub Releases** - Free, reliable for project assets
- **catbox.moe** - Quick file hosting, no account needed
  
## Browser Support

- Chromium based (like edge, brave, chrome)
- Firefox
- Safari
- Mobile browsers 

**Note:** Requires JavaScript enabled for full functionality

## Performance Notes

- Reduced particle count on mobile devices
- Passive event listeners for smooth scrolling
- RequestAnimationFrame for optimized animations
- Lazy loading for resources

## APIs Used

- **GitHub API** - Repository data
- **Lanyard API** - Discord presence
- **Simple Icons CDN** - Social media icons

## License

Free to use for personal portfolios. Please don't copy directly - use it as inspiration and make it your own.

## Credits

- Font: Chomsky (custom)
- Icons: [Simple Icons](https://simpleicons.org/)
- Discord Integration: [Lanyard](https://github.com/Phineas/lanyard)

---

**Note:** Remember to replace all placeholder URLs and IDs with your own information before deploying.
