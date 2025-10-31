# 🚀 Simple Deploy Guide

## TL;DR - Just Run These Commands:

```bash
npm run build
npm run deploy
```

**That's it!** Your site is now live at: https://arahmani25.github.io/ASR_Portfolio/

---

## 📝 Full Process (Step by Step)

### First Time Setup (Only Once)

```bash
# 1. Make sure you have the code
cd ASR_Portfolio

# 2. Install dependencies
npm install

# 3. Build the site
npm run build

# 4. Deploy to GitHub Pages
npm run deploy
```

**Wait 2-3 minutes**, then visit: https://arahmani25.github.io/ASR_Portfolio/

---

### Every Time You Make Changes

```bash
# 1. Test your changes locally
npm run dev
# Visit http://localhost:5173 to preview

# 2. When happy, build
npm run build

# 3. Deploy
npm run deploy
```

**Wait 2-3 minutes**, then refresh: https://arahmani25.github.io/ASR_Portfolio/

---

## 🎯 What Each Command Does

| Command | What It Does | When to Use |
|---------|--------------|-------------|
| `npm install` | Downloads dependencies | First time only, or after pulling new code |
| `npm run dev` | Runs local preview | Testing changes before deploying |
| `npm run build` | Creates production files | Before deploying |
| `npm run deploy` | Uploads to GitHub Pages | When ready to publish |

---

## 📂 What Actually Gets Deployed

**These files on your computer:**
```
App.tsx ❌ Not deployed
components/ ❌ Not deployed  
package.json ❌ Not deployed
```

**These files get deployed:**
```
dist/
├── index.html ✅ Deployed
├── assets/
│   ├── main.js ✅ Deployed (your React app, bundled)
│   └── app.css ✅ Deployed (your styles, compiled)
```

Only the `dist/` folder contents go to GitHub Pages!

---

## ✅ Checklist Before Deploying

- [ ] Made your changes
- [ ] Tested with `npm run dev`
- [ ] Dark mode works
- [ ] No console errors
- [ ] Ready to deploy

Then run:
```bash
npm run build && npm run deploy
```

---

## 🔄 GitHub Pages Auto-Update

After `npm run deploy`:
1. Files upload to GitHub (10 seconds)
2. GitHub Pages processes them (1-2 minutes)
3. Your site updates automatically
4. Clear cache (Ctrl+Shift+R) to see changes

---

## 💾 Saving Your Source Code (Optional but Recommended)

After deploying, save your source code too:

```bash
git add .
git commit -m "Updated portfolio"
git push origin main
```

This keeps your `.tsx` files and source code on GitHub so you can edit later!

---

## 🌐 Two URLs You Care About

1. **Live Site:** https://arahmani25.github.io/ASR_Portfolio/
   - This is what visitors see
   - Updates when you run `npm run deploy`

2. **Source Code:** https://github.com/arahmani25/ASR_Portfolio
   - This is your code
   - Updates when you run `git push`

---

## 🆘 Quick Troubleshooting

### Site not updating after deploy?
```bash
# Wait 2-3 minutes, then hard refresh:
# Windows: Ctrl + Shift + R
# Mac: Cmd + Shift + R
```

### Build errors?
```bash
# Clean and reinstall
rm -rf node_modules dist
npm install
npm run build
```

### Deploy errors?
```bash
# Make sure you committed changes first
git add .
git commit -m "Changes"
# Then deploy
npm run deploy
```

---

## 🎉 You're Done!

Every time you want to update your portfolio:

1. **Edit** your files
2. **Build** with `npm run build`
3. **Deploy** with `npm run deploy`
4. **Wait** 2-3 minutes
5. **Refresh** your live site

That's all! No server setup, no complicated hosting, just GitHub Pages! 🚀
