# Deployment Guide for Render

This guide will help you deploy your Flask portfolio website on Render for free.

## Prerequisites

1. A GitHub account
2. Your code pushed to a GitHub repository
3. A Render account (sign up at https://render.com)

## Step-by-Step Deployment Instructions

### Step 1: Prepare Your Code

✅ All files are already prepared:
- `requirements.txt` includes `gunicorn`
- `Procfile` is created
- `app.py` is configured for production

### Step 2: Push Code to GitHub

1. Initialize git repository (if not already done):
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Portfolio website"
   ```

2. Create a new repository on GitHub:
   - Go to https://github.com/new
   - Name it: `sharmin-portfolio` (or any name you prefer)
   - Don't initialize with README
   - Click "Create repository"

3. Push your code:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/sharmin-portfolio.git
   git branch -M main
   git push -u origin main
   ```
   Replace `YOUR_USERNAME` with your GitHub username.

### Step 3: Deploy on Render

1. **Sign up/Login to Render:**
   - Go to https://render.com
   - Sign up with your GitHub account (recommended for easy integration)

2. **Create New Web Service:**
   - Click "New +" button in the dashboard
   - Select "Web Service"
   - Click "Connect account" if you haven't connected GitHub yet
   - Select your repository: `sharmin-portfolio`

3. **Configure the Service:**
   - **Name:** `sharmin-portfolio` (or your preferred name)
   - **Environment:** `Python 3`
   - **Region:** Choose closest to you (e.g., Frankfurt, Singapore)
   - **Branch:** `main` (or `master` if that's your default branch)
   - **Root Directory:** Leave empty (default)
   - **Build Command:** `pip install -r requirements.txt`
   - **Start Command:** `gunicorn app:app`

4. **Add Environment Variables:**
   Click "Advanced" → "Add Environment Variable" and add:
   
   ```
   SECRET_KEY = (Click "Generate" or use a random string)
   MAIL_USERNAME = sharmin.chougule@gmail.com
   MAIL_PASSWORD = your-gmail-app-password
   MAIL_RECIPIENT = sharmin.chougule@gmail.com
   MAIL_SERVER = smtp.gmail.com
   MAIL_PORT = 587
   MAIL_USE_TLS = True
   ```
   
   **Important:** For Gmail, you need an App Password:
   - Go to Google Account → Security → 2-Step Verification → App passwords
   - Generate a password for "Mail"
   - Use that password (not your regular Gmail password)

5. **Deploy:**
   - Click "Create Web Service"
   - Wait 5-10 minutes for the first deployment
   - Your site will be live at: `https://sharmin-portfolio.onrender.com`

### Step 4: Verify Deployment

1. Visit your site URL
2. Test all sections:
   - Navigation works
   - Images load correctly
   - Contact form works (test sending a message)
   - All links work

### Step 5: Custom Domain (Optional)

If you want to use your own domain:

1. In Render dashboard → Your service → Settings → Custom Domain
2. Add your domain (e.g., `sharminchougule.com`)
3. Update DNS records:
   - Add a CNAME record:
     - Name: `@` or `www`
     - Value: `sharmin-portfolio.onrender.com`
   - Wait for DNS propagation (can take up to 48 hours)

## Troubleshooting

### Common Issues:

1. **Build fails:**
   - Check that `requirements.txt` is correct
   - Verify Python version (Render uses Python 3.11 by default)

2. **Site shows "Application Error":**
   - Check logs in Render dashboard
   - Verify `Procfile` is correct
   - Check that `gunicorn` is in requirements.txt

3. **Contact form doesn't work:**
   - Verify environment variables are set correctly
   - Check Gmail App Password is correct
   - Check Render logs for email errors

4. **Images not showing:**
   - Verify images are in `static/images/` folder
   - Check file names match exactly (case-sensitive)
   - Clear browser cache

### Viewing Logs:

- In Render dashboard → Your service → Logs
- This shows real-time application logs

## Free Tier Limitations

Render's free tier includes:
- ✅ Free SSL certificate
- ✅ Free subdomain
- ✅ 750 hours/month (enough for 24/7)
- ⚠️ Spins down after 15 minutes of inactivity (first request takes ~30 seconds)
- ⚠️ Can upgrade to paid plan for always-on service ($7/month)

## Next Steps After Deployment

1. Share your portfolio URL
2. Update your LinkedIn/resume with the portfolio link
3. Test the contact form regularly
4. Monitor Render dashboard for any issues

## Support

- Render Documentation: https://render.com/docs
- Render Support: support@render.com
- Check Render status: https://status.render.com

---

**Your site will be live at:** `https://sharmin-portfolio.onrender.com` (or your chosen name)

Good luck with your deployment! 🚀

