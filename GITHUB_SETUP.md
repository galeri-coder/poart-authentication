# GitHub Setup Instructions

## 🚀 Quick Upload to GitHub

### Step 1: Create GitHub Repository

1. Go to [github.com](https://github.com)
2. Click "New Repository"
3. Name: `ilhanart-poart-authentication`
4. Description: `Blockchain-based art authentication for Ali Naki İlhan collection`
5. **Public** repository
6. **DON'T** initialize with README (we already have one!)
7. Click "Create Repository"

### Step 2: Upload Files

**Option A: GitHub Web Interface (Easiest)**

1. On your new repo page, click "uploading an existing file"
2. Drag & drop the entire `github_repo` folder contents
3. Commit message: "Initial commit: PoArt Authentication System v1.0"
4. Click "Commit changes"

**Option B: Git Command Line**

Open terminal in the `github_repo` directory and run:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit: PoArt Authentication System v1.0"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/ilhanart-poart-authentication.git

# Push to GitHub
git branch -M main
git push -u origin main
```

**Replace `YOUR_USERNAME` with your actual GitHub username!**

---

## 📦 What's Being Uploaded?

```
Repository Contents (167 files):
├── 01_originals/              (32 files)
├── 02_original_hashes/        (32 files)
├── 03_watermarked/            (32 files)
├── 04_watermarked_hashes/     (32 files)
├── 05_metadata/               (32 files)
├── MASTER_AUTHENTICATION_RECORD.csv
├── README.md
├── LICENSE
├── CONTRIBUTING.md
└── .gitignore
```

**Total Size**: ~86 MB (mostly images)

---

## ⚠️ Important Notes

### Large Files
GitHub has a 100MB file size limit. All our files are under this limit. ✅

If you have files over 100MB in the future, use Git LFS:
```bash
git lfs install
git lfs track "*.png"
git add .gitattributes
```

### .gitignore
Already configured to ignore:
- Python cache files
- Temporary files
- IDE configs
- OS files

### Authentication Files
The repository includes:
- ✅ 32 watermarked images (safe to share)
- ✅ All SHA-512 hashes (public verification)
- ✅ JSON metadata (complete provenance)
- ✅ Master CSV (authentication record)

---

## 🔒 Security Best Practices

1. **Never commit**:
   - Private keys
   - API secrets
   - Personal information
   - Original unwatermarked images (if you want to keep them private)

2. **Keep watermarked versions public** for verification

3. **Master CSV is public** - it contains only hashes, not sensitive data

---

## 📝 After Upload

### Enable GitHub Pages (Optional)

1. Go to Settings → Pages
2. Source: Deploy from branch
3. Branch: main, folder: / (root)
4. Click Save
5. Your site will be at: `https://yourusername.github.io/ilhanart-poart-authentication`

### Add Topics

1. Go to repo home
2. Click ⚙️ next to "About"
3. Add topics:
   - `blockchain`
   - `art-authentication`
   - `nft`
   - `cryptography`
   - `poart`
   - `sha512`
   - `qr-code`

### Create Releases

1. Click "Releases" → "Create a new release"
2. Tag: `v1.0.0`
3. Title: `PoArt Authentication System v1.0`
4. Description: `Initial release - 32 authenticated artworks`
5. Attach the ZIP file
6. Publish release

---

## 🌟 Repository Features to Enable

- [x] README.md (Done!)
- [x] LICENSE (Done!)
- [x] .gitignore (Done!)
- [x] CONTRIBUTING.md (Done!)
- [ ] GitHub Pages (Optional)
- [ ] Issues tracking (Enable in Settings)
- [ ] Discussions (Enable in Settings)
- [ ] Wiki (Optional)

---

## 📊 Repository Settings

### General
- ✅ Template repository: NO
- ✅ Issues: ENABLED
- ✅ Preserve this repository: YES (important!)
- ✅ Sponsorships: Optional

### Branches
- Default branch: `main`
- Branch protection: Optional (for production)

### Actions
- GitHub Actions: Optional (for CI/CD)

---

## 🔗 Share Your Repository

After uploading, share:
- Repository URL: `https://github.com/YOUR_USERNAME/ilhanart-poart-authentication`
- Twitter: @Galerilhan
- Website: ilhanart.org

---

## 🎉 You're Done!

Your PoArt Authentication System is now on GitHub! 🚀

The repository serves as:
- ✅ Public authentication record
- ✅ Verification system
- ✅ Open-source reference
- ✅ Permanent archive

---

## 📞 Need Help?

- GitHub Docs: https://docs.github.com
- Git Tutorial: https://git-scm.com/docs/gittutorial
- Contact: ilhanart.org

---

**"Culture > Capital" 🎨**
