# BEE Korea Website

Welcome! This is the official website for BEE Korea (Biblical Education by Extension).

## 🌐 Live Site

The website is live at: [https://beekorea.org](https://beekorea.org)

## 📚 What is this?

This is a **static website** built with HTML, CSS, and JavaScript. It uses Bootstrap for styling and jQuery for interactivity. The site is available in both Korean and English.

## 🗂️ Project Structure

```
bee-web/
├── index.html              # Korean homepage
├── nav.html               # Shared navigation header
├── footer.html            # Shared footer
├── pages/                 # Korean content pages
│   └── NNN.html          # Numbered pages (001.html, 002.html, etc.)
├── en/                    # English version
│   ├── nav.html
│   └── pages/
├── css/                   # Stylesheets
├── js/                    # JavaScript files
├── images/                # Images and graphics
└── fonts/                 # Custom fonts
```

## 🚀 Deployment Workflow

This project uses **GitHub Pages** for automatic deployment. Here's how it works:

### Making Changes

1. **Edit files** locally using your preferred editor
2. **Test locally** by opening `index.html` in your browser (optional)
3. **Commit your changes:**
   ```bash
   git add .
   git commit -m "Brief description of changes"
   ```
4. **Push to GitHub:**
   ```bash
   git push github master
   ```

### Automatic Deployment

- GitHub Pages automatically builds and deploys when you push to the `master` branch
- Deployment takes 1-2 minutes
- Check deployment status: [GitHub Actions](https://github.com/BEEKorea/bee-web/actions)

## 🔗 Remote Repositories

This project is synced with two remote repositories:

- **`github`** - GitHub (used for deployment via GitHub Pages)
- **`origin`** - AWS CodeCommit (original repository)

**For deployments, only push to GitHub:**
```bash
git push github master
```

## 🛠️ Common Tasks

### Update a page
1. Find the page in `pages/` or `en/pages/`
2. Edit the HTML file
3. Commit and push to GitHub

### Add images
1. Place images in the `images/` folder
2. Reference them in HTML: `/images/your-image.png`
3. Commit and push

### Update navigation or footer
1. Edit `nav.html` or `footer.html`
2. Changes apply to all pages automatically
3. Commit and push

## 📝 Notes

- **Language parity**: If you update Korean content, consider updating the English version in `en/`
- **LMS integration**: The site includes links to `/lms/*` which connects to a separate Learning Management System
- **Cache busting**: The nav/footer includes version parameters to ensure fresh content loads

## 💡 Need Help?

- Check the [CLAUDE.md](./CLAUDE.md) file for detailed project guidelines
- Review recent commits for examples: `git log --oneline`
- Visit the live site to see your changes after deployment

---

Made with ❤️ by BEE Korea
