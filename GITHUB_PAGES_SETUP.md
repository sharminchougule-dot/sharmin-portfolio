# GitHub Pages Setup Guide

This guide will help you deploy your static portfolio website to GitHub Pages for free.

## Prerequisites

✅ Your code is already converted to static HTML/CSS/JS
✅ You have a GitHub account
✅ Your code is pushed to GitHub

## Step 1: Set Up EmailJS (Free Contact Form Service)

Since GitHub Pages doesn't support server-side code, we'll use EmailJS for the contact form.

1. **Sign up for EmailJS:**
   - Go to https://www.emailjs.com/
   - Sign up for a free account (free tier: 200 emails/month)

2. **Create an Email Service:**
   - Go to Email Services → Add New Service
   - Choose Gmail (or your email provider)
   - Connect your Gmail account
   - Note your Service ID (e.g., `service_xxxxx`)

3. **Create an Email Template:**
   - Go to Email Templates → Create New Template
   - Template ID will be generated (e.g., `template_xxxxx`)
   - Set up template variables:
     ```
     Subject: {{subject}}
     From: {{from_name}} <{{from_email}}>
     Message: {{message}}
     ```
   - Set "To Email" to: `sharmin.chougule@gmail.com`

4. **Get Your Public Key:**
   - Go to Account → General → API Keys
   - Copy your Public Key

5. **Update index.html:**
   - Open `index.html`
   - Find `YOUR_PUBLIC_KEY` and replace with your EmailJS Public Key
   - Find `YOUR_SERVICE_ID` and replace with your Service ID
   - Find `YOUR_TEMPLATE_ID` and replace with your Template ID

## Step 2: Enable GitHub Pages

1. **Go to your GitHub repository:**
   - Navigate to: https://github.com/sharminchougule-dot/sharmin-portfolio

2. **Enable GitHub Pages:**
   - Click "Settings" tab
   - Scroll down to "Pages" section (left sidebar)
   - Under "Source", select "Deploy from a branch"
   - Select branch: `main`
   - Select folder: `/ (root)`
   - Click "Save"

3. **Wait for deployment:**
   - GitHub will build and deploy your site
   - Usually takes 1-2 minutes
   - You'll see a green checkmark when done

4. **Your site will be live at:**
   - `https://sharminchougule-dot.github.io/sharmin-portfolio/`

## Step 3: Custom Domain (Optional)

If you want to use your own domain:

1. **In GitHub Pages Settings:**
   - Scroll to "Custom domain"
   - Enter your domain (e.g., `sharminchougule.com`)
   - Click "Save"

2. **Update DNS:**
   - Add a CNAME record:
     - Type: `CNAME`
     - Name: `@` or `www`
     - Value: `sharminchougule-dot.github.io`
   - Wait for DNS propagation (can take up to 48 hours)

## Step 4: Test Your Site

1. Visit your GitHub Pages URL
2. Test all sections:
   - Navigation works
   - Images load correctly
   - Contact form works (test sending a message)
   - All links work

## Troubleshooting

### Images Not Showing
- Check that image paths are correct: `static/images/filename.jpg`
- Verify images are committed to GitHub
- Check browser console for 404 errors

### Contact Form Not Working
- Verify EmailJS credentials are correct in `index.html`
- Check EmailJS dashboard for email logs
- Check browser console for JavaScript errors
- Make sure EmailJS SDK is loaded (check Network tab)

### Site Not Updating
- GitHub Pages can take a few minutes to update
- Hard refresh your browser (Ctrl+F5)
- Check GitHub Actions tab for build status

## File Structure for GitHub Pages

Your repository should have this structure:
```
sharmin-portfolio/
├── index.html          (main HTML file)
├── static/
│   ├── css/
│   │   └── style.css
│   └── images/
│       ├── profile-placeholder.jpeg
│       ├── publication-1.png
│       └── ...
└── README.md
```

## Benefits of GitHub Pages

✅ **Free hosting** - No cost
✅ **Free SSL** - HTTPS automatically enabled
✅ **Free subdomain** - `yourusername.github.io`
✅ **Easy updates** - Just push to GitHub
✅ **Fast CDN** - Fast loading worldwide
✅ **Version control** - Full Git history

## EmailJS Free Tier Limits

- 200 emails per month
- Perfect for a portfolio contact form
- Upgrade available if needed

## Next Steps

1. Set up EmailJS account
2. Update `index.html` with EmailJS credentials
3. Push changes to GitHub
4. Enable GitHub Pages
5. Share your portfolio URL!

---

**Your site will be live at:** `https://sharminchougule-dot.github.io/sharmin-portfolio/`

Good luck! 🚀

