# 🌌 Cosmos Portfolio

A modern, responsive personal portfolio designed for Physics students and Astronomy enthusiasts. Built with React, Tailwind CSS v4, and Framer Motion, featuring an interactive starfield background, spotlight card effects, and full light/dark mode support.

🔗 **Live Site:** [https://alinewaj.pro.bd](https://alinewaj.pro.bd)

## ✨ Features

-   **Dual Theme System:** Seamless Light/Dark mode toggle with persistent preference
-   **Interactive Starfield:** Canvas-based particle animation (auto-hides in light mode)
-   **Spotlight Cards:** Mouse-tracking radial gradient illumination on hover
-   **Content-Driven Architecture:** All text/data separated into `src/data.js` for easy editing
-   **Fully Responsive:** Mobile-first design with glassmorphism navigation
-   **Zero Terminal Deployment:** Designed to be managed entirely via GitHub Web Editor + Vercel
-   **Performance Optimized:** Vite build system with automatic code splitting

## 🎨 Design System

### Color Palette
| Token | Light Mode | Dark Mode | Usage |
|-------|-----------|-----------|-------|
| Background | `#ffffff` | `#0c0c0e` | Page base |
| Surface | `#ffffff` | `#18181b` | Cards, nav |
| Text Main | `#18181b` | `#f4f4f5` | Headings |
| Text Muted | `#71717a` | `#a1a1aa` | Body text |
| Border | `#e4e4e7` | `#27272a` | Dividers |
| Accent Primary | `#6F61C0` | `#A084E8` | Icons, focus |
| Accent Hover | `#A084E8` | `#8BE8E5` | Hover states |
| Accent Bright | `#8BE8E5` | `#8BE8E5` | Highlights |
| Accent Tag | `#D5FFE4` | `#6F61C0` | Badges |

### Typography
-   **Display:** Space Grotesk (headings, logo)
-   **Body:** Inter (paragraphs, UI elements)

## 📁 Project Structure

```
cosmos-portfolio/
├── public/
│   └── profile.jpg          # Your profile photo
├── src/
│   ├── data.js              # ✏️ ALL CONTENT EDITED HERE
│   ├── App.jsx              # Main application component
│   ├── index.css            # Theme variables & global styles
│   └── main.jsx             # Entry point
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

## 🚀 Deployment Guide

### Option A: Vercel (Recommended)

1.  Push this repository to GitHub
2.  Go to [vercel.com](https://vercel.com) → Sign in with GitHub
3.  Click **"Add New..." → Project**
4.  Import `cosmos-portfolio` → Framework preset auto-detects **Vite**
5.  Click **Deploy** → Live in ~30 seconds

### Custom Domain Setup (`Your Custom Domain`)

#### Step 1: Add Domain in Vercel
1.  Vercel Dashboard → Project → **Settings** → **Domains**
2.  Enter `Your Custom Domain` → Click **Add**
3.  Copy the TXT verification record value provided

#### Step 2: Configure DNS Records
At your DNS provider, add these records:

| Type | Name | Value | TTL |
|------|------|-------|-----|
| **TXT** | `_vercel` | `vc-domain-verify=your code,<your-code>` | 3600 |
| **A** | `@` | `76.76.21.21` | 3600 |

> ⚠️ **Note:** `.pro.bd` domains do not support CNAME at root. Use the A record above instead of the CNAME Vercel suggests. The TXT record is required for ownership verification since this domain was previously linked to another Vercel account.

#### Step 3: Verify
1.  Return to Vercel Domains page → Click **Refresh**
2.  Wait 5–15 minutes for ✅ green checkmark
3.  SSL certificate provisions automatically


## ✏️ Editing Content

All portfolio content lives in a single file: **`src/data.js`**

To update your site:
1.  Navigate to `src/data.js` on GitHub
2.  Click the ✏️ pencil icon
3.  Edit any field (name, bio, projects, education, volunteering, etc.)
4.  Click **Commit changes**
5.  Vercel auto-redeploys in ~30 seconds

### Adding Your Profile Photo
1.  Upload your photo to the `public/` folder via GitHub web (name it `profile.jpg`)
2.  In `src/data.js`, ensure: `profileImage: "/profile.jpg"`

### Adding Sections
-   **Education/Research:** Add entries to `EDUCATION` array with `type: "education"` or `type: "research"`
-   **Volunteering:** Add entries to `VOLUNTEERING` array
-   **Projects:** Add entries to `PROJECTS` array (`status: "Complete"` or `"In Progress"`)
-   **Skills:** Edit the `SKILLS` array

## 🛠️ Tech Stack

-   **React 19** – UI framework
-   **Vite 6** – Build tool & dev server
-   **Tailwind CSS v4** – Utility-first styling with `@theme` directives
-   **Framer Motion** – Scroll animations & AnimatePresence transitions
-   **Lucide React** – Icon library
-   **Vercel** – Hosting & automatic deployments

## 📄 License

MIT License — feel free to fork and customize for your own portfolio.
