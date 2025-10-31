# 🌟 Ahmad Shah Rahmani - Portfolio Website

[![Live Site](https://img.shields.io/badge/Live-Portfolio-blue?style=for-the-badge)](https://arahmani25.github.io/ASR_Portfolio/)
[![React](https://img.shields.io/badge/React-18.3-61DAFB?style=for-the-badge&logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.6-3178C6?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4.0-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)

> A stunning glassmorphism portfolio website with dark mode, smooth animations, and modern design aesthetics.

**🌐 Live Site:** [https://arahmani25.github.io/ASR_Portfolio/](https://arahmani25.github.io/ASR_Portfolio/)

---

## 🚀 Quick Start

### Deploy Your Portfolio in 3 Commands:

```bash
npm install           # Install dependencies
npm run build         # Build for production
npm run deploy        # Deploy to GitHub Pages
```

**That's it!** Your portfolio is now live! 🎉

Visit: [https://arahmani25.github.io/ASR_Portfolio/](https://arahmani25.github.io/ASR_Portfolio/)

---

## ✨ Features

- 🎨 **Glassmorphism Design** - Modern glass effect UI
- 🌓 **Dark Mode** - Smooth dark/light theme toggle with localStorage persistence
- ✨ **Smooth Animations** - Motion animations for engaging UX
- 📱 **Fully Responsive** - Works perfectly on all devices
- ⚡ **Optimized Performance** - Fast loading and smooth interactions
- 🎯 **SEO Friendly** - Meta tags and semantic HTML
- 🔒 **Type Safe** - Built with TypeScript
- 🎭 **Modern Stack** - React 18 + Tailwind CSS 4.0 + Vite

---

## 📋 Table of Contents

- [Quick Deploy](#quick-deploy)
- [Development](#development)
- [Project Structure](#project-structure)
- [Customization](#customization)
- [Guides](#guides)
- [Tech Stack](#tech-stack)
- [License](#license)

---

## 🚀 Quick Deploy

### First Time Setup:

```bash
# 1. Clone the repository
git clone https://github.com/arahmani25/ASR_Portfolio.git
cd ASR_Portfolio

# 2. Install dependencies
npm install

# 3. Build and deploy
npm run build
npm run deploy
```

### Update Content & Redeploy:

```bash
# 1. Edit your files (components, styles, etc.)

# 2. Test locally
npm run dev

# 3. Deploy changes
npm run build
npm run deploy
```

**Wait 2-3 minutes**, then visit your live site!

---

## 💻 Development

### Available Scripts:

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server at http://localhost:5173 |
| `npm run build` | Build for production (creates `dist/` folder) |
| `npm run preview` | Preview production build locally |
| `npm run deploy` | Deploy to GitHub Pages |

### Local Development:

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

Changes will hot-reload automatically! 🔥

---

## 📁 Project Structure

```
ASR_Portfolio/
├── components/              # React components
│   ├── Hero.tsx            # Hero section with animated background
│   ├── Navigation.tsx      # Navbar with dark mode toggle
│   ├── About.tsx           # About section
│   ├── Experience.tsx      # Work experience timeline
│   ├── Education.tsx       # Education timeline
│   ├── Projects.tsx        # Projects showcase
│   ├── Skills.tsx          # Skills with proficiency bars
│   ├── Awards.tsx          # Awards and achievements
│   ├── Contact.tsx         # Contact form
│   └── Footer.tsx          # Footer with social links
│
├── styles/
│   └── app.css             # Tailwind CSS + custom styles
│
├── App.tsx                 # Main app component
├── main.tsx                # Entry point
├── index.html              # HTML template
├── vite.config.ts          # Vite configuration
└── package.json            # Dependencies
```

---

## 🎨 Customization

### Update Your Information:

#### 1. Personal Info (Hero Section)
Edit `components/Hero.tsx`:
```tsx
export function Hero() {
  const socialLinks = [
    { icon: Mail, href: 'mailto:your@email.com', ... },
    { icon: Instagram, href: 'https://instagram.com/yourhandle', ... },
    // Add your links
  ];
  // ...
}
```

#### 2. Work Experience
Edit `components/Experience.tsx`:
```tsx
const experiences = [
  {
    company: 'Your Company',
    position: 'Your Position',
    period: 'Jan 2020 - Present',
    description: 'What you did...',
    achievements: ['Achievement 1', 'Achievement 2']
  },
  // Add more experiences
];
```

#### 3. Skills
Edit `components/Skills.tsx`:
```tsx
const skillCategories = [
  {
    category: 'Programming',
    skills: [
      { name: 'JavaScript', level: 90 },
      { name: 'Python', level: 85 },
      // Add your skills
    ]
  }
];
```

#### 4. Colors & Styling
Edit `styles/app.css`:
```css
@theme {
  --color-primary: #your-color;
  --color-secondary: #your-color;
}
```

### Change Dark Mode Behavior:
Edit `components/Navigation.tsx` - modify the `toggleDarkMode()` function.

---

## 📚 Guides

This project includes comprehensive guides to help you:

| Guide | Purpose |
|-------|---------|
| **[MASTER_GUIDE.md](./MASTER_GUIDE.md)** | 📖 Complete reference for everything |
| **[SIMPLE_DEPLOY_GUIDE.md](./SIMPLE_DEPLOY_GUIDE.md)** | 🚀 Quick deployment instructions |
| **[HOW_GITHUB_PAGES_WORKS.md](./HOW_GITHUB_PAGES_WORKS.md)** | 🧠 Understanding the deployment process |
| **[DEPLOY_VISUAL_GUIDE.md](./DEPLOY_VISUAL_GUIDE.md)** | 🎨 Visual diagrams of deployment |
| **[DARK_MODE_DEBUG.md](./DARK_MODE_DEBUG.md)** | 🌓 Dark mode troubleshooting |
| **[verify-build.md](./verify-build.md)** | ✅ Build verification checklist |

**👉 Start with [MASTER_GUIDE.md](./MASTER_GUIDE.md) for a complete overview!**

---

## 🛠️ Tech Stack

### Frontend Framework:
- **React 18.3** - UI library
- **TypeScript 5.6** - Type safety
- **Vite 6.0** - Build tool & dev server

### Styling:
- **Tailwind CSS 4.0** - Utility-first CSS framework
- **Motion (Framer Motion)** - Animation library
- **Custom CSS** - Glassmorphism effects

### UI Components:
- **Radix UI** - Accessible component primitives
- **Lucide React** - Icon library
- **Recharts** - Charts and graphs

### Deployment:
- **GitHub Pages** - Free static site hosting
- **gh-pages** - Deployment automation

---

## 🌐 How It Works

```
Your Computer                GitHub Pages              Visitor's Browser
     │                            │                           │
     │  1. npm run build          │                           │
     │  (Compile React)           │                           │
     │         │                  │                           │
     │         ↓                  │                           │
     │  dist/ folder created      │                           │
     │         │                  │                           │
     │  2. npm run deploy         │                           │
     │  (Upload files)            │                           │
     ├────────────────────────────→                           │
     │                            │                           │
     │                       Hosts files 24/7                 │
     │                            │                           │
     │                            │  3. User visits URL       │
     │                            ←───────────────────────────│
     │                            │                           │
     │                       Sends HTML/CSS/JS                │
     │                            ├───────────────────────────→
     │                            │                           │
     │                            │              4. React runs in browser
     │                            │              Shows portfolio ✨
```

**Key Point:** GitHub Pages is a **static file host**, not a server. Your React app runs entirely in the visitor's browser!

---

## 📊 Deployment Details

### What Gets Deployed:
- ✅ Compiled HTML (`index.html`)
- ✅ Optimized JavaScript (bundled React app)
- ✅ Compiled CSS (Tailwind + custom styles)
- ✅ Static assets (images, fonts)

### What Stays Local:
- ❌ Source `.tsx` files
- ❌ `node_modules/`
- ❌ Configuration files
- ❌ Development dependencies

Only the production-ready `dist/` folder is deployed!

---

## 🔧 Troubleshooting

### Site not updating?
```bash
# Hard refresh browser
Ctrl+Shift+R (Windows/Linux)
Cmd+Shift+R (Mac)
```

### Build errors?
```bash
# Clean install
rm -rf node_modules package-lock.json dist
npm install
npm run build
```

### Dark mode not working?
See [DARK_MODE_DEBUG.md](./DARK_MODE_DEBUG.md) for detailed troubleshooting.

---

## 📝 Updating Content

1. **Edit** the relevant component files
2. **Test** locally with `npm run dev`
3. **Build** with `npm run build`
4. **Deploy** with `npm run deploy`
5. **Wait** 2-3 minutes
6. **Refresh** your live site

---

## 🎯 Features Breakdown

### Hero Section
- Animated gradient background
- Floating orbs with motion animations
- Social media links
- Professional introduction

### Navigation
- Sticky navbar with glass effect
- Smooth scroll to sections
- Dark mode toggle (persists via localStorage)
- Responsive mobile menu

### Experience & Education
- Timeline layout
- Glassmorphism cards
- Smooth hover effects

### Projects
- Grid layout
- Tech stack tags
- Live demo & GitHub links

### Skills
- Categorized skill groups
- Visual proficiency bars
- Animated on scroll

### Contact
- Glass-styled form
- Email integration ready
- Social links

---

## 🌟 Highlights

- 🎨 **Modern Glassmorphism Design** - Beautiful glass effects throughout
- 🌓 **Persistent Dark Mode** - Saves preference across sessions
- ✨ **Smooth Animations** - Motion-powered transitions
- 📱 **Mobile-First Design** - Perfect on all screen sizes
- ⚡ **Fast Loading** - Optimized bundle size
- 🔍 **SEO Optimized** - Meta tags and semantic HTML
- ♿ **Accessible** - ARIA labels and keyboard navigation

---

## 📄 License

MIT License - See [LICENSE](./LICENSE) file for details.

---

## 👤 Author

**Ahmad Shah Rahmani**

- 📧 Email: ahmadshahrh@gmail.com
- 🌐 Website: [ahmadshahr.wordpress.com](https://ahmadshahr.wordpress.com)
- 📷 Instagram: [@iam_ahmad_rh](https://www.instagram.com/iam_ahmad_rh/)
- 📞 Phone: +7 980 207 66 68

---

## 🤝 Contributing

This is a personal portfolio, but feel free to:
- 🐛 Report bugs
- 💡 Suggest features
- 🍴 Fork and create your own version!

---

## 🎉 Acknowledgments

- Built with [React](https://reactjs.org/)
- Styled with [Tailwind CSS](https://tailwindcss.com/)
- Animated with [Motion](https://motion.dev/)
- Icons by [Lucide](https://lucide.dev/)
- Hosted on [GitHub Pages](https://pages.github.com/)

---

## 🚀 Get Started Now!

```bash
npm install && npm run build && npm run deploy
```

**Your portfolio will be live in minutes!** 🎊

Visit: [https://arahmani25.github.io/ASR_Portfolio/](https://arahmani25.github.io/ASR_Portfolio/)

---

<div align="center">

### ⭐ Star this repo if you found it helpful!

**Made with ❤️ by Ahmad Shah Rahmani**

</div>
