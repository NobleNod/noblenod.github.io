# 🎊 2025 Retrospective Website

A playful, mobile-friendly retrospective form that helps your friends reflect on 2025 and set intentions for 2026!

## Features

- ✨ Vibrant, colorful design with animated gradients
- 📱 Mobile-first, perfect for WhatsApp sharing
- 🎉 Satisfying confetti celebration on completion
- 📊 Automatic Google Sheets data collection
- 💚 One-tap WhatsApp sharing

## Quick Setup Guide

### Step 1: Set Up Google Sheets

1. Go to [Google Sheets](https://sheets.google.com) and create a new spreadsheet
2. Name it "2025 Retrospective Responses"
3. In Row 1, add these headers (one per column, starting from A1):

```
Timestamp | Name | Email | Letting Go | Burden Habit | Fear | Feeling In Way | Proud Of | Positive Influence | Secret Strength | Started Earlier | Health Goals | Skills/Hobbies | Places | Goals 2026 | Daily | Weekly | Monthly | Reminder When Stuck
```

### Step 2: Create the Google Apps Script

1. In your Google Sheet, go to **Extensions → Apps Script**
2. Delete any existing code
3. Copy ALL the code from `google-apps-script.js` and paste it
4. Click **Save** (Ctrl/Cmd + S)

### Step 3: Deploy the Script

1. Click **Deploy → New deployment**
2. Click the ⚙️ gear icon next to "Select type"
3. Choose **Web app**
4. Configure:
   - **Execute as:** Me
   - **Who has access:** Anyone
5. Click **Deploy**
6. Click **Authorize access** and follow the prompts
   - If you see "Google hasn't verified this app", click **Advanced → Go to [project name]**
7. **Copy the Web App URL** (looks like: `https://script.google.com/macros/s/XXXXX/exec`)

### Step 4: Connect the Form

1. Open `index.html`
2. Find this line near the bottom:
   ```javascript
   const GOOGLE_SCRIPT_URL = 'YOUR_GOOGLE_APPS_SCRIPT_URL_HERE';
   ```
3. Replace `YOUR_GOOGLE_APPS_SCRIPT_URL_HERE` with your Web App URL

### Step 5: Host the Website

**Option A: GitHub Pages (Free)**
1. Create a GitHub repository
2. Upload `index.html`
3. Go to Settings → Pages → Enable from main branch
4. Your site will be at `https://yourusername.github.io/repo-name`

**Option B: Netlify (Free)**
1. Go to [Netlify Drop](https://app.netlify.com/drop)
2. Drag and drop your `index.html` file
3. Get your instant URL

**Option C: Vercel (Free)**
1. Go to [Vercel](https://vercel.com)
2. Import your project
3. Deploy with one click

## Sharing on WhatsApp

Once hosted, the form includes a "Share with Friends" button that creates a pre-filled WhatsApp message with your link!

## Questions Covered

The form guides users through these reflection categories:

**🔍 Reflect (Questions 1-4)**
- What to let go of
- Burdensome habits
- Controlling fears
- Recurring feelings that get in the way

**🎉 Celebrate (Questions 5-7)**
- Proud moments from 2025
- Positive influences
- Secret sources of strength

**🌱 Grow (Questions 8-9, 14)**
- What to start earlier
- Health goals
- Personal mantras for tough times

**✨ Dream (Questions 10-13)**
- Skills/hobbies to explore
- Places to visit
- Goals for 2026
- Daily/weekly/monthly intentions

## Customization

**Change colors:** Edit the CSS variables at the top of the `<style>` section

```css
:root {
    --coral: #FF6B6B;
    --peach: #FFA07A;
    --sunshine: #FFD93D;
    /* etc... */
}
```

**Add questions:** Follow the existing card pattern in the HTML

**Modify the sharing message:** Edit the `shareOnWhatsApp()` function

---

Made with 💖 for reflecting on the journey
