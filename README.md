# Tiny Stamper

Simple landing page for a kid's Bitcoin side hustle — selling 3D printed seed phrase stamping blocks.

## Setup

### 1. Create GitHub Repo

```bash
cd tiny-stamper
git init
git add .
git commit -m "Initial commit: Tiny Stamper landing page"
gh repo create tiny-stamper --private --source=. --push
```

### 2. Enable GitHub Pages

1. Go to: **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** (or **master**)
4. Save

Your site will be live at: `https://YOURUSER.github.io/tiny-stamper/`

### 3. Custom Subdomain (stamps.bitcoin.com.au)

```bash
# Create CNAME file with your subdomain
echo "stamps.bitcoin.com.au" > CNAME
git add CNAME
git commit -m "Add custom subdomain"
git push
```

Then configure DNS at **Bitcoin.com.au**:

| Type | Name | Value |
|------|------|-------|
| CNAME | stamps | YOURUSER.github.io. |

*(Note: trailing dot is important)*

**Alternative A record approach:**

| Type | Name | Value |
|------|------|-------|
| A | stamps | 185.199.108.153 |
| A | stamps | 185.199.109.153 |
| A | stamps | 185.199.110.153 |
| A | stamps | 185.199.111.153 |

Wait ~1 hour for DNS to propagate, then visit: **https://stamps.bitcoin.com.au**

### 4. Customize Before Launch

| Task | File |
|------|------|
| YouTube embed | `index.html` |
| Lightning QR | `index.html` |
| On-chain QR | `index.html` |
| Telegram link | `index.html` |

**Generate QR codes:**
- Use **lnurlp** or **Lightningaddress.com** for Lightning QR
- Use your wallet for on-chain QR

## Files

- `index.html` — Main landing page
- `CNAME` — Custom subdomain
- `README.md` — Setup instructions

## Tech

- Tailwind CSS via CDN (no build step)
- Mobile-friendly
- Bitcoin orange theme
- Privacy-focused (no personal names publicly)
