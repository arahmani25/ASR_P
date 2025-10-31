# Build Verification Checklist

## Before Deploying

Run these commands in order:

### Step 1: Clean Everything
```bash
rm -rf node_modules package-lock.json dist
npm install
```

### Step 2: Test Local Dev Build
```bash
npm run dev
```
- Open http://localhost:5173
- Click dark mode toggle (moon/sun icon in top-right nav)
- Verify background changes from white to dark gray
- Check if text changes from dark to light
- Refresh page - dark mode should stay on

### Step 3: Test Production Build
```bash
npm run build
npm run preview
```
- Open the URL shown (usually http://localhost:4173)
- Test dark mode again
- Check browser console for errors

### Step 4: Deploy
```bash
npm run deploy
```

### Step 5: Verify on GitHub Pages
- Wait 2-3 minutes for deployment
- Visit: https://arahmani25.github.io/ASR_Portfolio/
- Test dark mode toggle
- Hard refresh (Ctrl+Shift+R) if needed

## What Dark Mode Should Do

### When Toggle is CLICKED:
1. ✅ Icon changes: Moon → Sun (light mode) or Sun → Moon (dark mode)
2. ✅ Background: White → Dark Gray (#111827)
3. ✅ Text: Dark → Light
4. ✅ Navigation: Light → Dark with glassmorphism effect
5. ✅ Cards/Sections: All should change colors

### After PAGE REFRESH:
1. ✅ Dark mode setting persists
2. ✅ No flash of light mode
3. ✅ Correct colors load immediately

## If Dark Mode STILL Doesn't Work

### Check 1: Is CSS Loading?
Open browser DevTools → Network tab → Reload page
- Look for `app.*.css` file
- Should show 200 status
- Click on it and verify it contains dark mode classes

### Check 2: Is JavaScript Working?
Open browser DevTools → Console tab
- Click dark mode toggle
- Should see no errors
- Run: `document.documentElement.classList`
  - Should show `dark` class when enabled

### Check 3: Is localStorage Working?
In Console, run:
```javascript
// Set dark mode
localStorage.setItem('darkMode', 'true')
document.documentElement.classList.add('dark')

// Check if it worked
localStorage.getItem('darkMode') // Should return 'true'
```

### Check 4: Cache Issues?
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Or open in incognito/private window
- Or clear browser cache completely

## Current Configuration Summary

✅ **CSS File**: `/styles/app.css` with Tailwind v4 dark mode
✅ **HTML Script**: Dark mode localStorage check in `<head>`
✅ **Toggle Logic**: In `/components/Navigation.tsx`
✅ **Dark Classes**: Throughout all components
✅ **Base Path**: `/ASR_Portfolio/` for GitHub Pages

## Files to Check After Build

After running `npm run build`, verify these files exist in `dist/`:
- `index.html` (should have dark mode script)
- `assets/app-[hash].css` (should contain dark mode styles)
- `assets/main-[hash].js` (should contain React app)

You can preview what's in dist by running:
```bash
ls -la dist/
ls -la dist/assets/
```
