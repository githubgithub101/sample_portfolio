# How to Publish Your Portfolio Website to GitHub Pages

This guide will walk you through the complete process of publishing your portfolio website to GitHub Pages, starting from creating a GitHub account to accessing your live website.

---

## Table of Contents
1. [Creating a GitHub Account](#step-1-creating-a-github-account)
2. [Installing Git (if needed)](#step-2-installing-git)
3. [Creating a New Repository](#step-3-creating-a-new-repository)
4. [Preparing Your Files](#step-4-preparing-your-files)
5. [Uploading Files to GitHub](#step-5-uploading-files-to-github)
6. [Enabling GitHub Pages](#step-6-enabling-github-pages)
7. [Accessing Your Live Website](#step-7-accessing-your-live-website)
8. [Updating Your Website](#step-8-updating-your-website)
9. [Troubleshooting](#troubleshooting)

---

## Step 1: Creating a GitHub Account

### 1.1 Visit GitHub
1. Open your web browser
2. Go to **https://github.com**
3. Click the **"Sign up"** button in the top-right corner

### 1.2 Fill Out Registration Form
1. **Enter your email address**
   - Use a valid email you have access to
   - Example: `yourname@example.com`

2. **Create a password**
   - Must be at least 15 characters OR at least 8 characters with a number and lowercase letter
   - Example: `MySecurePassword123!`

3. **Choose a username**
   - This will be part of your website URL
   - Must be unique (not already taken)
   - Use lowercase letters, numbers, or hyphens
   - Example: `juandelacruz` or `juan-delacruz`
   - **IMPORTANT:** Your website URL will be: `https://yourusername.github.io/repository-name`

4. **Email preferences**
   - Choose whether you want to receive product updates (optional)

5. **Verify you're human**
   - Complete the CAPTCHA puzzle

6. Click **"Create account"**

### 1.3 Verify Your Email
1. Check your email inbox
2. Find the email from GitHub
3. Click the verification link in the email
4. You'll be redirected to GitHub

### 1.4 Complete Your Profile (Optional but Recommended)
1. Click your profile icon in the top-right corner
2. Select **"Settings"**
3. Add:
   - Profile picture
   - Bio
   - Location
   - Website (you can add this later after publishing)

---

## Step 2: Installing Git

### For Windows:
1. Go to **https://git-scm.com/download/win**
2. Download the installer
3. Run the installer
4. Use default settings (just keep clicking "Next")
5. Click "Finish"

### For macOS:
**Option 1: Using Homebrew (Recommended)**
```bash
brew install git
```

**Option 2: Download Installer**
1. Go to **https://git-scm.com/download/mac**
2. Download and install

### For Linux (Ubuntu/Debian):
```bash
sudo apt-get update
sudo apt-get install git
```

### Verify Installation
Open Terminal (Mac/Linux) or Command Prompt (Windows) and type:
```bash
git --version
```
You should see something like: `git version 2.x.x`

### Configure Git (First Time Only)
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

---

## Step 3: Creating a New Repository

### 3.1 Create Repository on GitHub
1. **Log in to GitHub** (if not already logged in)
2. Click the **"+"** icon in the top-right corner
3. Select **"New repository"**

### 3.2 Repository Settings
1. **Repository name:**
   - Enter a name for your project
   - Example: `portfolio-website` or `juan-delacruz-portfolio`
   - **IMPORTANT:** Use lowercase and hyphens (no spaces)
   - This will be part of your URL: `https://yourusername.github.io/repository-name`

2. **Description (Optional):**
   - Example: "My personal portfolio website showcasing my projects and skills"

3. **Visibility:**
   - Choose **"Public"** (required for free GitHub Pages)
   - Private repositories require GitHub Pro for Pages

4. **Initialize repository:**
   - ☐ Do NOT check "Add a README file"
   - ☐ Do NOT add .gitignore
   - ☐ Do NOT choose a license
   - (We'll add files manually)

5. Click **"Create repository"**

### 3.3 Copy Repository URL
After creating, you'll see a page with setup instructions.
- Look for the **HTTPS URL**
- It will look like: `https://github.com/yourusername/repository-name.git`
- Keep this page open or copy the URL

---

## Step 4: Preparing Your Files

### 4.1 Verify File Structure
Make sure your portfolio folder has this structure:

```
module6_delacruz/
│
├── index.html
├── about.html
├── projects.html
├── contact.html
│
├── css/
│   └── styles.css
│
└── images/
    ├── profile.jpg
    ├── project1.jpg
    ├── project2.jpg
    └── project3.jpg
```

### 4.2 Test Your Website Locally
1. Navigate to your project folder
2. Double-click `index.html`
3. Test all links:
   - Click all navigation menu items
   - Verify all pages load correctly
   - Check that images display
   - Test responsiveness (resize browser window)

### 4.3 Important File Checks
- ✅ `index.html` MUST be in the root folder (not in a subfolder)
- ✅ All file names are lowercase
- ✅ No spaces in file or folder names
- ✅ All links use relative paths (not absolute paths)
- ✅ CSS file is linked correctly in all HTML files

---

## Step 5: Uploading Files to GitHub

### Method 1: Using Git Command Line (Recommended)

#### 5.1 Open Terminal/Command Prompt
- **Windows:** Open Command Prompt or Git Bash
- **Mac/Linux:** Open Terminal

#### 5.2 Navigate to Your Project Folder
```bash
cd path/to/your/module6_delacruz
```

Example:
```bash
# Windows
cd C:\Users\YourName\Documents\module6_delacruz

# Mac/Linux
cd ~/Documents/module6_delacruz
```

#### 5.3 Initialize Git Repository
```bash
git init
```
You should see: `Initialized empty Git repository`

#### 5.4 Add All Files
```bash
git add .
```
The dot (.) means "add all files in current folder"

#### 5.5 Commit Your Files
```bash
git commit -m "Initial commit - Portfolio website"
```

#### 5.6 Connect to GitHub Repository
Replace with YOUR GitHub repository URL:
```bash
git remote add origin https://github.com/yourusername/repository-name.git
```

Example:
```bash
git remote add origin https://github.com/juandelacruz/portfolio-website.git
```

#### 5.7 Rename Branch to Main (if needed)
```bash
git branch -M main
```

#### 5.8 Push Files to GitHub
```bash
git push -u origin main
```

You'll be asked to log in:
1. Enter your GitHub username
2. For password, you need a **Personal Access Token** (not your GitHub password)

**Creating a Personal Access Token:**
1. Go to GitHub.com
2. Click your profile picture → Settings
3. Scroll down → Click "Developer settings" (left sidebar)
4. Click "Personal access tokens" → "Tokens (classic)"
5. Click "Generate new token" → "Generate new token (classic)"
6. Give it a name: "Git Access"
7. Select expiration: 90 days (or your preference)
8. Check the box for **"repo"** (full control of private repositories)
9. Click "Generate token"
10. **COPY THE TOKEN IMMEDIATELY** (you won't see it again)
11. Use this token as your password when pushing

---

### Method 2: Using GitHub Desktop (Easier for Beginners)

#### 5.1 Download GitHub Desktop
1. Go to **https://desktop.github.com/**
2. Download for your operating system
3. Install and open GitHub Desktop
4. Sign in with your GitHub account

#### 5.2 Add Your Repository
1. Click **"File"** → **"Add Local Repository"**
2. Click **"Choose..."** and select your project folder
3. If it says "not a git repository," click **"Create a repository"**

#### 5.3 Make Initial Commit
1. You'll see all your files listed
2. In the bottom left:
   - Summary: "Initial commit"
   - Description (optional): "Added portfolio website files"
3. Click **"Commit to main"**

#### 5.4 Publish to GitHub
1. Click **"Publish repository"** (top bar)
2. Confirm the name
3. Make sure **"Keep this code private"** is UNCHECKED
4. Click **"Publish repository"**

---

### Method 3: Upload Directly via GitHub Website (Simplest)

#### 5.1 Go to Your Repository
1. Log in to GitHub
2. Go to your repository page
3. You should see the empty repository page

#### 5.2 Upload Files
1. Click **"uploading an existing file"** link
   (Or click "Add file" → "Upload files")

2. **Drag and drop** your project folder OR click **"choose your files"**
   - Select ALL files and folders:
     - index.html
     - about.html
     - projects.html
     - contact.html
     - css folder
     - images folder

3. Wait for upload to complete (you'll see green checkmarks)

4. At the bottom:
   - Commit message: "Initial commit"
   - Click **"Commit changes"**

**IMPORTANT for Method 3:**
- GitHub website upload has file size limits
- Large files may not upload
- If you have many files, Method 1 or 2 is better

---

## Step 6: Enabling GitHub Pages

### 6.1 Access Repository Settings
1. Go to your repository on GitHub
2. You should see all your files listed
3. Click **"Settings"** tab (top-right area)

### 6.2 Navigate to Pages Settings
1. In the left sidebar, scroll down
2. Click **"Pages"** (under "Code and automation")

### 6.3 Configure GitHub Pages
1. **Source section:**
   - Branch: Select **"main"** (or "master" if that's what you have)
   - Folder: Select **"/ (root)"**
   - Click **"Save"**

2. Wait a moment (the page will refresh)

3. You'll see a message:
   > "Your site is ready to be published at `https://yourusername.github.io/repository-name/`"

4. After 1-2 minutes, refresh the page
   - The message will change to:
   > "Your site is live at `https://yourusername.github.io/repository-name/`"
   - The box will turn green

### 6.4 Custom Domain (Optional)
If you have a custom domain:
1. In the "Custom domain" field, enter your domain
2. Click "Save"
3. Configure DNS settings with your domain provider

---

## Step 7: Accessing Your Live Website

### 7.1 Get Your Website URL
Your website URL will be:
```
https://yourusername.github.io/repository-name/
```

**Example:**
- Username: `juandelacruz`
- Repository: `portfolio-website`
- URL: `https://juandelacruz.github.io/portfolio-website/`

### 7.2 Visit Your Website
1. Open a new browser tab
2. Type your GitHub Pages URL
3. Press Enter
4. Your portfolio should load!

### 7.3 Test Everything
- ✅ Check all pages load (Home, About, Projects, Contact)
- ✅ Test navigation menu
- ✅ Verify images display
- ✅ Test links
- ✅ Check responsive design (resize browser or use phone)

### 7.4 Share Your Website
You can now share your website URL with:
- Friends and family
- Potential employers
- On your resume
- On social media
- In your email signature

---

## Step 8: Updating Your Website

When you want to make changes to your website:

### Using Git Command Line:
```bash
# 1. Navigate to your project folder
cd path/to/your/module6_delacruz

# 2. Make your changes to the files (edit HTML/CSS)

# 3. Add the changes
git add .

# 4. Commit the changes
git commit -m "Updated about page"

# 5. Push to GitHub
git push origin main

# 6. Wait 1-2 minutes, then refresh your website
```

### Using GitHub Desktop:
1. Make changes to your files
2. Open GitHub Desktop
3. You'll see the changed files
4. Enter commit message
5. Click "Commit to main"
6. Click "Push origin"
7. Wait 1-2 minutes, refresh your website

### Using GitHub Website:
1. Go to your repository
2. Navigate to the file you want to edit
3. Click the pencil icon (✏️) to edit
4. Make changes
5. Scroll down, enter commit message
6. Click "Commit changes"
7. Wait 1-2 minutes, refresh your website

---

## Troubleshooting

### Problem: Website shows 404 error
**Solutions:**
1. Check that GitHub Pages is enabled (Settings → Pages)
2. Verify the branch is set to "main" and folder is "/ (root)"
3. Make sure `index.html` is in the root folder (not in a subfolder)
4. Wait 5-10 minutes after enabling Pages
5. Clear browser cache (Ctrl+F5 or Cmd+Shift+R)

### Problem: CSS not loading (page has no styling)
**Solutions:**
1. Check CSS file path in HTML:
   ```html
   <link rel="stylesheet" href="css/styles.css">
   ```
2. Make sure `styles.css` is in the `css` folder
3. Check for typos in folder/file names
4. All folder and file names should be lowercase
5. Hard refresh browser (Ctrl+F5)

### Problem: Images not showing
**Solutions:**
1. Check image file paths:
   ```html
   <img src="images/profile.jpg" alt="...">
   ```
2. Verify image files are in the `images` folder
3. Check image file extensions (.jpg, .png, .svg)
4. File names are case-sensitive (profile.jpg ≠ Profile.jpg)
5. Make sure images were uploaded to GitHub

### Problem: Changes not appearing on live site
**Solutions:**
1. Wait 2-5 minutes after pushing changes
2. Clear browser cache:
   - Chrome/Edge: Ctrl+Shift+Delete (Windows) or Cmd+Shift+Delete (Mac)
   - Or use Incognito/Private mode
3. Check that changes were committed and pushed to GitHub
4. Verify you're looking at the correct URL

### Problem: "Permission denied" when pushing
**Solutions:**
1. Make sure you're using a Personal Access Token (not password)
2. Create a new token if the old one expired
3. Check that you have write access to the repository

### Problem: Links between pages not working
**Solutions:**
1. Use relative paths:
   - ✅ GOOD: `<a href="about.html">`
   - ❌ BAD: `<a href="C:/Users/name/about.html">`
2. Check for typos in file names
3. All HTML files should be in the same folder (root)

### Problem: Website works locally but not on GitHub Pages
**Solutions:**
1. Check all file paths are relative (not absolute)
2. Verify all file names are lowercase
3. Remove any spaces from file/folder names
4. Check that all files were uploaded to GitHub
5. Look at browser console for errors (F12 → Console tab)

---

## Additional Tips

### Best Practices:
1. **Test locally first** before pushing to GitHub
2. **Write clear commit messages** describing what you changed
3. **Commit often** - don't wait to commit all changes at once
4. **Keep a backup** of your website files locally
5. **Use meaningful file names** that describe the content

### Security:
1. Never commit sensitive information (passwords, API keys)
2. Don't include personal information you want to keep private
3. Remember: public repositories are visible to everyone

### Performance:
1. Optimize images (compress before uploading)
2. Keep file sizes reasonable
3. Minimize CSS and remove unused styles

### SEO (Search Engine Optimization):
1. Use descriptive page titles
2. Add meta descriptions to each page:
   ```html
   <meta name="description" content="Portfolio of Juan Dela Cruz, Computer Science Student">
   ```
3. Use semantic HTML tags
4. Add alt text to all images

---

## Useful Commands Reference

### Git Commands:
```bash
# Check status of files
git status

# See commit history
git log

# See what changes you made
git diff

# Undo changes (before commit)
git checkout -- filename.html

# Pull latest changes from GitHub
git pull origin main

# Clone a repository
git clone https://github.com/username/repo.git
```

### Checking Git Configuration:
```bash
# View all settings
git config --list

# Check username
git config user.name

# Check email
git config user.email
```

---

## Resources

### Official Documentation:
- **GitHub Docs:** https://docs.github.com/
- **GitHub Pages:** https://pages.github.com/
- **Git Documentation:** https://git-scm.com/doc

### Learning Resources:
- **GitHub Learning Lab:** https://lab.github.com/
- **Git Tutorial (Atlassian):** https://www.atlassian.com/git/tutorials
- **GitHub Skills:** https://skills.github.com/

### Video Tutorials:
- Search YouTube for: "GitHub Pages tutorial"
- Search YouTube for: "How to use Git and GitHub"

---

## Congratulations! 🎉

You've successfully published your portfolio website to GitHub Pages!

Your website is now:
- ✅ Live and accessible worldwide
- ✅ Free to host (thanks to GitHub)
- ✅ Easily updateable
- ✅ Shareable via a professional URL

### Next Steps:
1. Share your website URL with friends and instructors
2. Add the link to your resume or CV
3. Keep updating and improving your portfolio
4. Add new projects as you complete them
5. Consider getting a custom domain name

**Remember:** Your portfolio is a living document. Keep it updated with your latest work and skills!

---

**Need Help?**
- Check the Troubleshooting section
- Search GitHub Docs
- Ask your instructor
- Search Stack Overflow
- Check GitHub Community Forums

Good luck with your portfolio! 🚀