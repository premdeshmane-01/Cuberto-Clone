# Cuberto Agency Clone - Interactive Digital Agency Website

A pixel-perfect recreation of Cuberto's award-winning digital agency website, featuring advanced GSAP animations, WebGL effects, and interactive media elements. This project showcases modern frontend development techniques and creative interaction design.

## 🎯 Project Overview

This is a production-grade recreation of a leading digital agency's portfolio website, demonstrating expertise in:
- Advanced animation libraries (GSAP, ScrollTrigger)
- WebGL shader effects using Shery.js
- Smooth scrolling interactions
- Responsive design principles
- Custom cursor effects

## ✨ Key Features

### Interactive Elements
- **Custom Mouse Follower**: Dynamic cursor that follows mouse movement
- **Magnetic Elements**: Interactive elements with magnetic hover effects
- **Video Hover Cards**: Hover over headings to reveal full-motion video backgrounds
- **Image Effects**: WebGL-powered image distortion effects on scroll

### Advanced Animations
- **Scroll-Triggered Animations**: Pinned sections with smooth vertical scrolling
- **Parallax Effects**: Multi-layered scrolling for depth perception
- **Synchronized Image Gallery**: Images change based on scroll position
- **GSAP Timeline**: Professional-grade animation sequencing

### Design Features
- Clean, minimalist aesthetic
- Typography-focused design
- Smooth transitions and micro-interactions
- Professional color palette and spacing

## 🛠️ Technologies & Libraries

### Core Technologies
- **HTML5**: Semantic structure
- **CSS3**: Advanced styling with custom properties
- **JavaScript (ES6+)**: Modern syntax and features

### Animation Libraries
- **GSAP 3.12.2**: Industry-standard animation library
- **ScrollTrigger**: Scroll-based animation control
- **Shery.js**: WebGL effects and interactive media

### Additional Libraries
- **Three.js**: 3D graphics and WebGL rendering
- **ControlKit**: Real-time parameter control
- **Remix Icon**: Modern icon set

## 📁 Project Structure

```
cuberto-clone/
│
├── index.html          # Main HTML structure
├── style.css           # Core styling and layout
├── script.js           # Animation and interaction logic
│
├── media/
│   ├── 0.mp4           # Hover video 1
│   ├── 2.mp4           # Hover video 2
│   └── 3.mp4           # Hover video 3
│
└── README.md           # Project documentation
```

## 🚀 Getting Started

### Prerequisites
- Modern web browser with WebGL support
- Local development server (recommended)
- Basic understanding of JavaScript

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/cuberto-clone.git
cd cuberto-clone
```

2. **Add video files**
Place your video files (0.mp4, 2.mp4, 3.mp4) in the project root

3. **Start a local server**
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx http-server

# Using VS Code Live Server
# Right-click index.html → Open with Live Server
```

4. **Open in browser**
Navigate to `http://localhost:8000`

## 💻 Code Breakdown

### 1. Mouse Follower Effect
```javascript
Shery.mouseFollower();
```
Creates a custom cursor that smoothly follows mouse movement

### 2. Magnetic Elements
```javascript
Shery.makeMagnet(".magnet");
```
Applies magnetic hover effect to navigation and buttons

### 3. Video Hover Effect
```javascript
Shery.hoverWithMediaCircle(".hvr", {
  videos: ["./0.mp4", "./2.mp4", "./3.mp4"],
});
```
Displays video in circular mask on hover over heading elements

### 4. Scroll-Pinned Animation
```javascript
gsap.to(".fleftelm", {
  scrollTrigger: {
    trigger: "#fimages",
    pin: true,              // Pins the section
    start: "top top",
    end: "bottom bottom",
    scrub: 1,               // Smooth scrubbing
  },
  y: "-300%",
  ease: Power1,
});
```
Pins featured section and animates text vertically while scrolling

### 5. Synchronized Image Gallery
```javascript
Shery.imageEffect(".images", {
  style: 4,
  slideStyle: (setScroll) => {
    sections.forEach(function (section, index) {
      ScrollTrigger.create({
        trigger: section,
        onUpdate: function (prog) {
          setScroll(prog.progress + index);
        },
      });
    });
  },
});
```
Syncs image transitions with scroll-triggered text sections

## 🎨 Design System

### Typography
- **Primary Font**: Averta CY W10
- **Heading Sizes**: 1.34vw - 7vw (responsive)
- **Letter Spacing**: Tight (-8px to -1px)

### Color Palette
```css
Background: #ffffff
Primary Text: #000000
Stroke Text: transparent with 1px stroke
Selection: #000000 background, #ffffff text
Accents: #f7f7f7, #e6e6e6
```

### Spacing System
- Consistent use of viewport units (vw)
- Padding: 5vw - 15vw for sections
- Margins: 1.5vw - 5vw for elements

## 🎯 Key Sections

### 1. Hero Section
- Large headline with stroke text effect
- Interactive video hover on keywords
- Minimalist navigation

### 2. Featured Projects
- Scroll-pinned gallery
- Synchronized text and images
- WebGL distortion effects

### 3. Resources Section
- Course cards with hover effects
- Clean grid layout
- Call-to-action buttons

## ⚡ Performance Optimizations

- Efficient GSAP animations using `will-change`
- Optimized scroll listeners with `scrub`
- Lazy-loaded WebGL effects
- Minimal DOM manipulation
- Hardware-accelerated CSS transforms

## 📱 Responsive Design

The website is fully responsive with:
- Viewport-based units (vw, vh)
- Flexible layouts
- Adaptive typography
- Touch-friendly interactions

## 🔧 Customization Guide

### Change Video Files
Replace video paths in `script.js`:
```javascript
Shery.hoverWithMediaCircle(".hvr", {
  videos: ["./your-video-1.mp4", "./your-video-2.mp4", "./your-video-3.mp4"],
});
```

### Modify Scroll Animation
Adjust animation parameters in `script.js`:
```javascript
gsap.to(".fleftelm", {
  y: "-300%",        // Change scroll distance
  ease: Power1,      // Change easing function
});
```

### Update Image Effect Style
Change Shery.js effect style (1-6):
```javascript
Shery.imageEffect(".images", {
  style: 4,  // Try styles 1-6
});
```

### Customize Colors
Update CSS variables in `style.css`:
```css
background-color: #fff;      /* Main background */
-webkit-text-stroke: 1px #000; /* Stroke text */
```

## 🎓 Learning Outcomes

This project demonstrates proficiency in:
- ✅ Advanced GSAP animation techniques
- ✅ ScrollTrigger implementation
- ✅ WebGL shader effects
- ✅ Custom cursor interactions
- ✅ Scroll-based storytelling
- ✅ Production-grade code organization
- ✅ Performance optimization
- ✅ Modern ES6+ JavaScript

## 🐛 Known Issues & Solutions

### Issue: Videos not playing on hover
**Solution**: Ensure video files are in the correct path and use supported formats (MP4, WebM)

### Issue: ScrollTrigger not working
**Solution**: Check GSAP and ScrollTrigger are loaded in correct order

### Issue: WebGL effects not displaying
**Solution**: Verify browser supports WebGL and GPU acceleration is enabled

## 📚 Resources & Documentation

- [GSAP Documentation](https://greensock.com/docs/)
- [ScrollTrigger Docs](https://greensock.com/docs/v3/Plugins/ScrollTrigger)
- [Shery.js GitHub](https://github.com/aayushchouhan24/sheryjs)
- [Three.js Documentation](https://threejs.org/docs/)

## 🤝 Contributing

This is a learning project for portfolio purposes. Feedback and suggestions are welcome!

## 📄 License

This project is for educational purposes only. Original design by Cuberto Agency.

## 👨‍💻 Developer

**Created by**: Prem Deshmane  
**Purpose**: Frontend development portfolio piece  
**Skills Demonstrated**: React, GSAP, WebGL, Modern JavaScript, Responsive Design

---

### 💡 Note
This is a recreation project built to demonstrate frontend development skills, particularly in:
- Complex animation implementation
- Advanced JavaScript libraries
- Production-grade code quality
- Attention to detail in UI/UX

**Original Website**: [Cuberto Agency](https://cuberto.com)
