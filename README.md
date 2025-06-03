Enhanced Anti-Screenshot Protection


🌟 Overview
A comprehensive client-side solution to deter unauthorized screenshots and screen captures across multiple platforms including Windows, macOS, Android, and iOS.

Live Demo
License

✨ Features
Cross-Platform Protection
#Windows: Blocks Print Screen, Win+Shift+S, Alt+PrintScreen

#macOS: Blocks Cmd+Shift+3, Cmd+Shift+4, Cmd+Shift+5

#Android/iOS: Detects app switching and blurs content

Multiple Protection Layers
Context menu (right-click) disabled

Keyboard shortcuts blocked

Content blurring on window/tab switch

Dynamic noise overlay to degrade screenshot quality

Developer tools detection

User Experience
Visual glitch effects on detection

Status indicators showing protection is active

Warning notifications for detected attempts

Beautiful responsive UI

🚀 Getting Started
Basic Implementation
Add this code to your HTML file:

```<!-- Anti-screenshot protection -->
<script>
    // Enhanced keyboard shortcut blocking
    document.addEventListener('keydown', function(e) {
        // Windows/Linux PrintScreen
        if (e.key === 'PrintScreen' || e.keyCode === 44) {
            e.preventDefault();
            triggerGlitch();
        }
        
        // Windows Win+Shift+S
        if (e.key === 's' && e.shiftKey && (e.metaKey || e.ctrlKey)) {
            e.preventDefault();
            triggerGlitch();
        }
        
        // macOS screenshot shortcuts
        if (e.metaKey && e.shiftKey && (e.key === '3' || e.key === '4' || e.key === '5')) {
            e.preventDefault();
            triggerGlitch();
        }
    });

    // Add noise overlay
    function addNoiseOverlay() {
        const noise = document.createElement('div');
        noise.id = 'noiseOverlay';
        noise.style.background = `url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='1' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)' opacity='0.1'/%3E%3C/svg%3E")`;
        document.body.appendChild(noise);
    }
    
    // Initialize
    addNoiseOverlay();
</script>```

##Full Implementation
#For complete protection with all features, use the full code provided in the solution above.

🛡️ ##How It Works
The script uses a combination of techniques to protect content:

Event Listeners

contextmenu: Prevents right-click context menu

keydown: Detects and blocks screenshot-related keyboard shortcuts

visibilitychange: Blurs content when the page/tab is hidden

blur/focus: Handles window focus changes

Platform Detection

```javascript

const isWindows = navigator.platform.indexOf('Win') > -1;
const isMac = navigator.platform.indexOf('Mac') > -1;
const isIOS = /iPad|iPhone|iPod/.test(navigator.userAgent);
const isAndroid = /Android/.test(navigator.userAgent);
```

Visual Deterrents

Dynamic noise overlay (SVG-based)

Glitch animation on detection events

Content blurring when window loses focus

Mobile-Specific Protections

Detects multi-touch gestures

Uses page visibility API to protect content when app is backgrounded

🌐 Browser Support
Browser	Windows	macOS	Android	iOS
Chrome	✅	✅	✅	✅
Firefox	✅	✅	✅	✅
Safari	N/A	✅	N/A	✅
Edge	✅	✅	✅	✅
⚠️ Security Disclaimer
Important: While this solution significantly increases protection against casual screenshots, no client-side solution can provide 100% protection against determined attackers. Physical cameras, specialized software, and browser extensions can bypass these protections. This should be used as a deterrent, not as a foolproof security measure.

🧪 Testing the Protection
Try these actions to see the protection in action:

Press Print Screen (Windows/Linux)

Press Win+Shift+S (Windows)

Press Cmd+Shift+4 (macOS)

Switch to another app or tab

Open developer tools (F12 or Ctrl+Shift+I)

Right-click anywhere on the page

📁 Project Structure
anti-screenshot-protection/
├── index.html                # Main implementation
├── README.md                 # This documentation
├── assets/                   # Additional resources
│   ├── css/
│   │   └── styles.css        # Additional styles
│   └── img/                  # Project images
└── examples/                 # Usage examples
    ├── basic.html            # Minimal implementation
    └── full-protection.html  # Complete solution

🤝 ##Contributing
Contributions are welcome! Please follow these steps:

Fork the project

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

📜 ##License
Distributed under the MIT License. See LICENSE for more information.

✉️ ##Contact
Project Maintainer - [Lovsan] - [lovster6@gmail.com]

Project Link: https://github.com/Lovsan/anti-screenshot-protection

Protect your content with cutting-edge client-side security! 🔒

