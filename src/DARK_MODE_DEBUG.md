# Dark Mode Debugging Guide

## How Dark Mode Works in Your Portfolio

### 1. **Files Involved**
- `/styles/app.css` - Main CSS with Tailwind v4 dark mode configuration
- `/components/Navigation.tsx` - Dark mode toggle button and logic
- `/index.html` - Script that loads saved dark mode preference immediately
- `/App.tsx` - Root component with dark mode classes

### 2. **How It Works**
1. **Initial Load**: Script in `index.html` checks `localStorage.getItem('darkMode')` and adds `.dark` class to `<html>` before React loads
2. **Toggle**: Clicking the moon/sun icon in navigation calls `toggleDarkMode()` which:
   - Updates state
   - Saves preference to localStorage
   - Adds/removes `.dark` class on `<html>`
3. **Styling**: All Tailwind classes with `dark:` prefix automatically activate when `.dark` class is present

### 3. **Testing Dark Mode Locally**

Before deploying, test locally:

```bash
# Install dependencies
npm install

# Start dev server
npm run dev
```

Open http://localhost:5173 and:
1. Click the moon icon in the top-right
2. Check if colors change
3. Refresh the page - dark mode should persist
4. Open browser DevTools Console and run:
   ```javascript
   localStorage.getItem('darkMode') // Should return 'true' or 'false'
   document.documentElement.classList.contains('dark') // Should return true/false
   ```

### 4. **Common Issues & Solutions**

#### Issue: Dark mode doesn't activate when clicking toggle
**Solution**: Check browser console for errors. Make sure:
- No JavaScript errors
- `document.documentElement.classList` is working
- localStorage is not disabled

#### Issue: Dark mode doesn't persist after refresh
**Solution**: 
- Clear browser cache
- Check if localStorage is enabled in browser
- Verify the script in `index.html` is running

#### Issue: Some elements don't change color
**Solution**: 
- Check if the component has `dark:` classes
- Verify CSS is loading correctly
- Run: `npm run build && npm run preview` to test production build

### 5. **Deploy Steps**

```bash
# 1. Clean install
rm -rf node_modules package-lock.json
npm install

# 2. Build
npm run build

# 3. Test build locally
npm run preview

# 4. If everything works, deploy
npm run deploy
```

### 6. **Verify on GitHub Pages**

After deployment (wait 2-3 minutes):
1. Visit: https://arahmani25.github.io/ASR_Portfolio/
2. Open DevTools (F12)
3. Go to Console tab
4. Test dark mode toggle
5. Check localStorage:
   ```javascript
   localStorage.getItem('darkMode')
   ```

### 7. **Emergency Fix**

If dark mode still doesn't work after deployment:

1. Check if Tailwind CSS is loading:
   ```javascript
   // In browser console
   getComputedStyle(document.body).getPropertyValue('--color-gray-900')
   ```

2. Manually test dark class:
   ```javascript
   // In browser console
   document.documentElement.classList.add('dark')
   ```

3. If manual toggle works but button doesn't, check Navigation component for errors

### 8. **Browser Compatibility**

Dark mode should work in:
- ✅ Chrome/Edge (v90+)
- ✅ Firefox (v88+)
- ✅ Safari (v14+)
- ✅ Mobile browsers

### 9. **Cache Issues**

If you see old styling:
1. Hard refresh: `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac)
2. Clear site data in DevTools
3. Try incognito/private browsing mode
