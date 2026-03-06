## Updated File Structure & CSS References

### Root Directory Files

**index.html** (Main Portfolio Page)
```
├── CSS Reference: <link rel="stylesheet" href="assets/css/style.css">
├── Image Reference: <img src="assets/images/avatar.jpg">
├── Navigation Links:
│   ├── [home] - #about (anchor link)
│   ├── [cv] - cv.pdf (external PDF)
│   ├── [blog] - blog/ (folder)
│   ├── [travels] - Instagram (external)
│   └── [links] - links.html
└── Sections: About, Projects, Work Experience, Conference Travels
```

**links.html** (Useful Resources)
```
├── CSS Reference: <link rel="stylesheet" href="assets/css/style.css">
├── Navigation Links:
│   └── [home] - index.html#
├── Sections:
│   ├── Recommended Courses
│   ├── Free eBooks
│   └── AI Tools I Use
└── Format: Links with title, source, and [visit] button
```

### Blog Directory Files

**blog/index.html** (Blog Main Page)
```
├── CSS Reference: <link rel="stylesheet" href="../assets/css/style.css">
├── Navigation Links:
│   ├── [home] - ../ (parent directory)
│   └── [links] - ../links.html
├── Sections:
│   ├── Latest Articles (with links to posts)
│   └── Topics (keyword directory)
└── Format: Article title, date, excerpt, [read article] link
```

**blog/first-post.html** (Sample Blog Post)
```
├── CSS Reference: <link rel="stylesheet" href="../assets/css/style.css">
├── Navigation Links:
│   ├── [home] - ../
│   ├── [blog] - ./
│   └── [links] - ../links.html
├── Content Sections:
│   ├── Post Header (title + metadata)
│   ├── Post Content (paragraphs + headings)
│   └── Post Footer (published date + back link)
└── Format: Full article with H2 subheadings and bullet lists
```

### Assets Directory

**assets/css/style.css**
```
├── Global Styles (reset, typography, layout)
├── Navigation Styles (.site-nav)
├── Header Styles (.page-header, .avatar)
├── Content Styles (.content-section, headings)
├── List Styles (.projects-list, .experience-list, .travels-list, .links-list, .blog-list, .topic-list)
├── Blog Post Styles (.blog-post, .post-header, .post-content, .post-list, .post-footer)
├── Link Styles (all link colors and hover states)
├── Footer Styles
└── Mobile Responsive (@media max-width: 600px)
```

**assets/images/avatar.jpg**
```
├── Size: 252px × 252px (desktop)
├── Format: JPG/PNG
├── Style: Border-radius 50% (circular)
├── Border: 1px solid #f0f0f0
├── Mobile Size: 150px × 150px
└── Note: Replace with your own profile photo
```

**assets/icons/favicon.ico**
```
├── Format: ICO or PNG
├── Size: 32x32 or 64x64 pixels
├── Location: Used by browsers automatically
└── Note: Add your favicon to this location
```

### CSS Path Reference Table

| File Location | CSS Path |
|---|---|
| `/index.html` | `assets/css/style.css` |
| `/links.html` | `assets/css/style.css` |
| `/blog/index.html` | `../assets/css/style.css` |
| `/blog/first-post.html` | `../assets/css/style.css` |

### Image Path Reference Table

| File Location | Image Path |
|---|---|
| `/index.html` | `assets/images/avatar.jpg` |
| `/blog/index.html` | `../assets/images/avatar.jpg` (if needed) |
| `/blog/first-post.html` | `../assets/images/avatar.jpg` (if needed) |

### Navigation Link Reference Table

| From Page | To Page | Link |
|---|---|---|
| `/index.html` | Blog | `blog/` |
| `/index.html` | Links | `links.html` |
| `/links.html` | Home | `index.html#` |
| `/blog/index.html` | Home | `../` |
| `/blog/index.html` | Links | `../links.html` |
| `/blog/first-post.html` | Home | `../` |
| `/blog/first-post.html` | Blog | `./` |
| `/blog/first-post.html` | Links | `../links.html` |

## Design System Summary

### Typography
- **Primary Font:** Source Serif Pro
- **Persian Font:** Vazirmatn
- **Base Size:** 14pt (desktop), 13pt (mobile)
- **Heading Weight:** 700 (bold)
- **Body Weight:** 400 (regular)

### Color Palette
- **Primary Link:** #0096FF
- **Link Hover:** #0078CC
- **Primary Text:** #1a1a1a
- **Secondary Text:** #555-#666
- **Borders:** #eaeaea
- **Background:** #fff

### Layout Specifications
- **Max Width:** 2560px
- **Desktop Margins:** 120px left/right
- **Mobile Margins:** 20px left/right
- **Mobile Breakpoint:** 600px
- **Section Padding:** 3% top/bottom (.top-buffer)

### Visual Elements
- **Bullet Style:** ▪ (small square)
- **Bullet Size:** 1.2em (desktop), 1em (mobile)
- **Item Indent:** 28px
- **Border Style:** 1px solid #eaeaea
- **Avatar Style:** 252x252px (desktop), 150x150px (mobile), 50% border-radius

## Important Notes

1. **Relative Paths:** Blog files use `../` to reference parent directory
2. **Folder Navigation:** Blog folder index with `/` auto-loads `index.html`
3. **Single CSS File:** All pages share one `style.css` for consistency
4. **Responsive:** Mobile adjustments at 600px breakpoint
5. **No Duplicates:** Each HTML file exists in only one location
6. **Asset Organization:** All static files in `assets/` folder

## Deployment Instructions

1. Push entire folder structure to GitHub
2. Enable GitHub Pages in repository settings
3. Set source to `main` branch (or your branch)
4. Site will be available at: `https://ewazfakor.github.io/`
5. All internal links will work correctly with the relative path structure