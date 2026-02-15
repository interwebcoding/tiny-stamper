# Blake's Bitcoin Blocks

Simple landing page for Blake's Bitcoin side hustle — selling 3D printed seed phrase stamping blocks.

## Setup

### 1. Create GitHub Repo

```bash
cd blakes-bitcoin-blocks
git init
git add .
git commit -m "Initial commit: Blake's Bitcoin Blocks landing page"
gh repo create blakes-bitcoin-blocks --public --source=. --push
```

### 2. Enable GitHub Pages

1. Go to: **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** (or **gh-pages**)
4. Save

Your site will be live at: `https://YOURUSER.github.io/blakes-bitcoin-blocks/`

### 3. Custom Subdomain (blocks.bitcoin.com.au)

```bash
# Create CNAME file with YOUR subdomain
echo "blocks.bitcoin.com.au" > CNAME
git add CNAME
git commit -m "Add custom subdomain"
git push
```

Then configure DNS at **Bitcoin.com.au**:

| Type | Name | Value |
|------|------|-------|
| CNAME | blocks | YOURUSER.github.io. |

*(Note: trailing dot is important)*

**Alternative A record approach:**

| Type | Name | Value |
|------|------|-------|
| A | blocks | 185.199.108.153 |
| A | blocks | 185.199.109.153 |
| A | blocks | 185.199.110.153 |
| A | blocks | 185.199.111.153 |

Wait ~1 hour for DNS to propagate, then visit: **https://blocks.bitcoin.com.au**

### 4. Customize

- **Video:** Replace the video placeholder div with your YouTube embed
- **QR Codes:** Generate real Lightning/on-chain QR codes
- **Telegram Link:** Update the Telegram group link
- **Prices:** Update BTC price range if needed

## Files

- `index.html` — Main landing page
- `CNAME` — Custom domain (optional)

## Tech

- Tailwind CSS via CDN (no build step)
- Mobile-friendly
- Bitcoin orange theme
