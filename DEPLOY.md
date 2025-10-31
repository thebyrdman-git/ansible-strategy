# Deploy to GitHub Pages

## Step 1: Create GitHub Repository

1. Go to: https://github.com/new
2. **Repository name:** `ansible-strategy`
3. **Description:** "Visual guide to ansibleizing everything - work and life automation with Ansible"
4. **Public** repository (required for free GitHub Pages)
5. **DO NOT** initialize with README (we already have files)
6. Click **Create repository**

## Step 2: Push to GitHub

```bash
cd /home/jbyrd/repos/ansible-strategy

# Add GitHub remote
git remote add origin git@github.com:thebyrdman-git/ansible-strategy.git

# Push to GitHub
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository: https://github.com/thebyrdman-git/ansible-strategy
2. Click **Settings** (top right)
3. Click **Pages** (left sidebar)
4. Under "Build and deployment":
   - **Source:** Deploy from a branch
   - **Branch:** main
   - **Folder:** / (root)
5. Click **Save**

## Step 4: Wait for Deployment

GitHub Pages takes 1-2 minutes to build and deploy.

**Your site will be live at:**
```
https://thebyrdman-git.github.io/ansible-strategy/
```

## Step 5: Test the Site

Visit the URL and verify:
- ✅ Draw.io diagram loads and is interactive
- ✅ All sections render correctly
- ✅ Links work (GitLab, GitHub, blog)
- ✅ Responsive design (test on mobile)

## Optional: Custom Domain

If you want to use `ansible.jbyrd.org`:

1. Add CNAME record in Cloudflare:
   - **Type:** CNAME
   - **Name:** ansible
   - **Target:** thebyrdman-git.github.io
   - **Proxy status:** DNS only (orange cloud OFF)

2. Create `CNAME` file in repo:
   ```bash
   echo "ansible.jbyrd.org" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

3. In GitHub Settings → Pages → Custom domain:
   - Enter: `ansible.jbyrd.org`
   - Click **Save**
   - Wait for DNS check

## Troubleshooting

**Draw.io diagram not loading?**
- Wait 5 minutes for GitHub Pages to fully deploy
- Check browser console for errors
- Verify the raw GitHub URL is accessible

**404 error?**
- GitHub Pages is still building (wait 2-3 minutes)
- Check that main branch is selected in Settings → Pages

**Styling looks broken?**
- Hard refresh: Ctrl+Shift+R (Windows/Linux) or Cmd+Shift+R (Mac)
- Clear browser cache

---

**Status:** Ready to deploy ✅  
**Files:** 4 (README.md, index.html, ansibleize-everything.drawio, DEPLOY.md)  
**Branch:** main  
**Ready for:** GitHub Pages deployment

