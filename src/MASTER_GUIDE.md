# 🎯 MASTER GUIDE - Your Complete Portfolio Reference

## 📋 Table of Contents
1. [Quick Deploy](#quick-deploy)
2. [How It Works](#how-it-works)
3. [Your Portfolio Structure](#your-portfolio-structure)
4. [Common Tasks](#common-tasks)
5. [Troubleshooting](#troubleshooting)

---

## 🚀 Quick Deploy

### Deploy Your Portfolio NOW:
```bash
npm run build
npm run deploy
```

**Your live site:** https://arahmani25.github.io/ASR_Portfolio/

### Deploy + Save Source Code:
```bash
npm run build
npm run deploy
git add .
git commit -m "Updated portfolio"
git push origin main
```

---

## 🧠 How It Works

### The Magic Explained Simply:

```
┌─────────────────────────────────────────────────────────────┐
│ YOUR COMPUTER                                               │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. You edit .tsx files                                    │
│  2. Run: npm run build                                     │
│     → Compiles React → Plain HTML/CSS/JS                   │
│     → Saves to dist/ folder                                │
│                                                             │
│  3. Run: npm run deploy                                    │
│     → Uploads dist/ folder to GitHub                       │
│                                                             │
└─────────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────────┐
│ GITHUB PAGES (Cloud)                                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. Receives your files                                    │
│  2. Hosts them 24/7 (FREE)                                 │
│  3. Serves to anyone who visits your URL                   │
│                                                             │
└─────────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────────┐
│ VISITOR'S BROWSER                                           │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  1. Downloads HTML/CSS/JS                                  │
│  2. Runs React code IN THE BROWSER                         │
│  3. Sees your beautiful portfolio 🎨                       │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Key Points:
- ✅ GitHub Pages = **Static File Host** (NOT a server)
- ✅ React runs **in the visitor's browser** (client-side)
- ✅ You need Node.js **only on your computer** (for building)
- ✅ Completely **FREE** hosting
- ✅ Works **24/7** without your computer running

---

## 📁 Your Portfolio Structure

### Source Files (On Your Computer - `main` branch):
```
ASR_Portfolio/
├── components/          ← Your React components (.tsx)
│   ├── Hero.tsx
│   ├── Navigation.tsx
│   ├── About.tsx
│   └── ...
├── styles/
│   └── app.css         ← Your Tailwind CSS
├── App.tsx             ← Main React component
├── main.tsx            ← Entry point
├── package.json        ← Dependencies
└── vite.config.ts      ← Build configuration
```

### Built Files (Deployed to `gh-pages` branch):
```
dist/                    ← Created by "npm run build"
├── index.html          ← Your compiled app
├── assets/
│   ├── main-abc123.js  ← React + your code (bundled)
│   └── app-xyz789.css  ← Styles (compiled)
└── vite.svg            ← Static assets
```

**Only `dist/` folder gets deployed to GitHub Pages!**

---

## 🛠️ Common Tasks

### 1️⃣ Test Locally (Before Deploying)
```bash
npm run dev
```
- Opens: http://localhost:5173
- See changes in real-time
- Press `Ctrl+C` to stop

### 2️⃣ Deploy to Live Site
```bash
npm run build    # Compile everything
npm run deploy   # Upload to GitHub Pages
```
- Wait 2-3 minutes
- Visit: https://arahmani25.github.io/ASR_Portfolio/
- Hard refresh: `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac)

### 3️⃣ Update Content

**Edit any file** (e.g., `components/Hero.tsx`):
```tsx
// Change your name, title, links, etc.
export function Hero() {
  return (
    <div>
      <h1>Your New Title</h1>
    </div>
  );
}
```

**Then deploy:**
```bash
npm run build
npm run deploy
```

### 4️⃣ Change Dark Mode Behavior

Edit `/components/Navigation.tsx`:
```tsx
const toggleDarkMode = () => {
  // Your custom logic here
};
```

### 5️⃣ Add New Section

1. Create new component: `components/NewSection.tsx`
2. Import in `App.tsx`:
   ```tsx
   import { NewSection } from './components/NewSection';
   ```
3. Add to render:
   ```tsx
   <NewSection />
   ```
4. Deploy:
   ```bash
   npm run build && npm run deploy
   ```

### 6️⃣ Update Skills/Experience/Projects

Edit the respective component files:
- **Skills**: `components/Skills.tsx`
- **Experience**: `components/Experience.tsx`
- **Projects**: `components/Projects.tsx`
- **Education**: `components/Education.tsx`

Then deploy!

---

## 🔧 Troubleshooting

### Problem: Site shows old content after deploy

**Solution:**
```bash
# 1. Clear browser cache
Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)

# 2. Or open in incognito/private window

# 3. Or wait 5 minutes and try again
```

### Problem: Dark mode not working

**Solution:**
1. Check console for errors (F12 → Console)
2. Verify script in `index.html` exists
3. Test toggle in DevTools:
   ```javascript
   document.documentElement.classList.add('dark')
   ```
4. See `DARK_MODE_DEBUG.md` for detailed steps

### Problem: Build errors

**Solution:**
```bash
# Clean everything
rm -rf node_modules package-lock.json dist

# Fresh install
npm install

# Try building again
npm run build
```

### Problem: Deploy errors

**Solution:**
```bash
# Make sure gh-pages is installed
npm install gh-pages --save-dev

# Try deploying again
npm run deploy

# If still fails, check GitHub repo settings:
# Settings → Pages → Source should be "gh-pages branch"
```

### Problem: 404 Error on GitHub Pages

**Solution:**
1. Check `vite.config.ts` has correct base path:
   ```typescript
   base: '/ASR_Portfolio/'  // Match your repo name
   ```
2. Rebuild and redeploy:
   ```bash
   npm run build
   npm run deploy
   ```

### Problem: CSS not loading

**Solution:**
1. Check `main.tsx` imports CSS:
   ```typescript
   import "./styles/app.css";
   ```
2. Verify `styles/app.css` exists
3. Rebuild:
   ```bash
   npm run build
   ```

---

## 📊 Understanding Your Branches

Your GitHub repo has TWO branches:

### `main` (or `master`) Branch
- **What:** Source code
- **Contains:** `.tsx` files, `package.json`, configs
- **Who sees:** Developers looking at your code
- **Update with:**
  ```bash
  git add .
  git commit -m "Updated code"
  git push origin main
  ```

### `gh-pages` Branch
- **What:** Built/compiled files
- **Contains:** `index.html`, `.js`, `.css` from `dist/`
- **Who sees:** Visitors to your live site
- **Update with:**
  ```bash
  npm run deploy
  ```
  (Automatic, don't push manually)

---

## 🎨 Customization Guide

### Change Colors

Edit `styles/app.css`:
```css
@theme {
  --color-primary: #your-color;
}
```

### Change Fonts

Edit `styles/app.css`:
```css
@import url('https://fonts.googleapis.com/css2?family=YourFont&display=swap');

body {
  font-family: 'YourFont', sans-serif !important;
}
```

### Change Animation Speed

Edit `styles/app.css`:
```css
.gradient-bg {
  animation: gradient 10s ease infinite; /* Change 10s */
}
```

---

## 📞 Important Files Quick Reference

| File | Purpose | When to Edit |
|------|---------|-------------|
| `App.tsx` | Main app structure | Add/remove sections |
| `components/*.tsx` | Individual sections | Change content |
| `styles/app.css` | Styles & colors | Change appearance |
| `vite.config.ts` | Build settings | Change base path |
| `package.json` | Dependencies | Add libraries |
| `index.html` | HTML template | Add meta tags |

---

## 🎯 Quick Commands Reference

| Command | What It Does | When to Use |
|---------|--------------|-------------|
| `npm install` | Install dependencies | First time setup |
| `npm run dev` | Start local preview | Testing changes |
| `npm run build` | Build for production | Before deploying |
| `npm run deploy` | Deploy to GitHub Pages | Publish changes |
| `npm run preview` | Preview production build | Test before deploy |

---

## ✅ Pre-Deploy Checklist

Before running `npm run deploy`:

- [ ] Tested locally with `npm run dev`
- [ ] Dark mode toggle works
- [ ] All links work
- [ ] No console errors
- [ ] Content is updated
- [ ] Animations working
- [ ] Mobile responsive

Then:
```bash
npm run build && npm run deploy
```

---

## 🌐 Your URLs

1. **Live Portfolio:** https://arahmani25.github.io/ASR_Portfolio/
   - What visitors see
   - Updates after `npm run deploy`

2. **GitHub Repo:** https://github.com/arahmani25/ASR_Portfolio
   - Your source code
   - Updates after `git push`

3. **Local Dev:** http://localhost:5173
   - Only when running `npm run dev`
   - Only on your computer

---

## 📚 Additional Resources

- **`SIMPLE_DEPLOY_GUIDE.md`** - Quick deploy reference
- **`HOW_GITHUB_PAGES_WORKS.md`** - Detailed explanation
- **`DARK_MODE_DEBUG.md`** - Dark mode troubleshooting
- **`verify-build.md`** - Build verification checklist

---

## 🎉 You're All Set!

### Remember:
1. **Edit** source files on your computer
2. **Test** with `npm run dev`
3. **Build** with `npm run build`
4. **Deploy** with `npm run deploy`
5. **Enjoy** your live portfolio! 🚀

### Need Help?
- Check the troubleshooting section above
- Read the additional guides
- All your code is backed up on GitHub

**Happy coding!** 💻✨
