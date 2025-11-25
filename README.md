# Cookie Consent System - GitHub Installation Guide

## 📦 What You're Getting

A complete, production-ready cookie consent system that:
- ✅ Actually blocks tracking scripts (not cosmetic)
- ✅ GDPR, CCPA, and globally compliant
- ✅ Styled with your website's CSS variables
- ✅ 2-second delayed load
- ✅ Manages: GA4, GTM, Google Ads, Facebook, LinkedIn, HubSpot

---

## 🚀 Quick Start (3 Steps)

### **Step 1: Upload Files to GitHub**

1. Create a new repository (or use existing):
   ```
   https://github.com/YOUR-USERNAME/YOUR-REPO
   ```

2. Upload these 2 files:
   - `cookie-consent.min.css`
   - `cookie-consent.min.js`

3. Go to **Settings → Pages**
4. Enable **GitHub Pages** (choose `main` branch)
5. Your files will be available at:
   ```
   https://YOUR-USERNAME.github.io/YOUR-REPO/cookie-consent.min.css
   https://YOUR-USERNAME.github.io/YOUR-REPO/cookie-consent.min.js
   ```

---

### **Step 2: Add to Webflow (Single Line!)**

Go to **Webflow → Project Settings → Custom Code → Head Code**

Paste this **ONE LINE**:

```html
<link rel="stylesheet" href="https://YOUR-USERNAME.github.io/YOUR-REPO/cookie-consent.min.css"><script src="https://YOUR-USERNAME.github.io/YOUR-REPO/cookie-consent.min.js" defer></script>
```

**Replace:**
- `YOUR-USERNAME` with your GitHub username
- `YOUR-REPO` with your repository name

**That's it!** 🎉

---

### **Step 3: Configure Tracking IDs**

Edit `cookie-consent.min.js` on GitHub and replace:

1. **Google Analytics 4:**
   ```javascript
   // Find: YOUR-GA4-ID
   // Replace with: G-XXXXXXXXXX
   ```

2. **Facebook Pixel:**
   ```javascript
   // Find: YOUR-FACEBOOK-PIXEL-ID
   // Replace with: 123456789012345
   ```

3. **LinkedIn Insight Tag:**
   ```javascript
   // Find: YOUR-LINKEDIN-ID
   // Replace with: 1234567
   ```

**Commit changes** and they'll update automatically on your site!

---

## 🎨 Customization

### **Change Banner Delay**
Edit `cookie-consent.min.js`:
```javascript
// Find: bannerDelay:2e3
// Change to: bannerDelay:5000 (for 5 seconds)
```

### **Change Privacy Policy URL**
Edit `cookie-consent.min.js`:
```javascript
// Find: privacyPolicyUrl:"/privacy-policy"
// Change to: privacyPolicyUrl:"/your-url"
```

### **Change Button Text**
Edit `cookie-consent.min.js` - search for button text and replace.

---

## 📊 File Sizes

- **CSS:** ~8KB minified (~2KB gzipped)
- **JS:** ~15KB minified (~5KB gzipped)
- **Total:** ~23KB (~7KB gzipped)

Super lightweight! ⚡

---

## ✅ Testing Checklist

After installation:
1. ☐ Clear browser cookies
2. ☐ Reload page
3. ☐ Wait 2 seconds - banner should appear
4. ☐ Click "Accept All" - check GA4 real-time reports
5. ☐ Click "Reject All" - verify no tracking scripts load
6. ☐ Test cookie settings button (bottom-left)
7. ☐ Test on mobile device

---

## 🔧 Troubleshooting

### **Banner doesn't appear?**
1. Check browser console for errors
2. Verify GitHub Pages is enabled
3. Check file URLs are correct
4. Clear browser cache

### **Tracking not working?**
1. Verify you replaced placeholder IDs
2. Check browser console for consent status
3. Test in GTM preview mode

### **Styling looks wrong?**
1. Make sure your CSS variables are defined
2. Check that stylesheet loads before script
3. Verify no CSS conflicts

---

## 🌐 CDN Alternative (jsDelivr)

Instead of GitHub Pages, you can use jsDelivr for faster global CDN:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/YOUR-USERNAME/YOUR-REPO@main/cookie-consent.min.css">
<script src="https://cdn.jsdelivr.net/gh/YOUR-USERNAME/YOUR-REPO@main/cookie-consent.min.js" defer></script>
```

Benefits:
- ✅ Faster (global CDN)
- ✅ Auto-caching
- ✅ HTTPS by default

---

## 📝 What Gets Blocked

The system automatically blocks these patterns:
- `google-analytics.com/analytics.js`
- `googletagmanager.com/gtag/js`
- `googletagmanager.com/gtm.js`
- `googleadservices.com`
- `connect.facebook.net`
- `snap.licdn.com`
- `js.hs-analytics.net`

Until user gives consent! 🔒

---

## 🎯 Advanced: Using Multiple Sites

If you want to use this on multiple websites:

1. Keep files in GitHub (one place)
2. Use the same link on all sites:
   ```html
   <link rel="stylesheet" href="https://YOUR-USERNAME.github.io/cookie-consent/cookie-consent.min.css">
   <script src="https://YOUR-USERNAME.github.io/cookie-consent/cookie-consent.min.js" defer></script>
   ```
3. Update once, applies everywhere!

---

## 📞 Support

If you run into issues:
1. Check browser console for error messages
2. Verify all placeholder IDs are replaced
3. Test with browser cache cleared
4. Check GitHub Pages is enabled

---

## 🎉 You're Done!

Your cookie consent system is now:
- ✅ Hosted on GitHub (free, fast, reliable)
- ✅ Loaded with 1 line in Webflow
- ✅ Fully functional and compliant
- ✅ Easy to update (just edit on GitHub)

**Enjoy your privacy-compliant website!** 🚀
