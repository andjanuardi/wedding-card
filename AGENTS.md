# AGENTS.md

## Critical Distinctions From Typical Web Apps

This project is **NOT** a structured Node.js/framework project. It's a **single HTML file** with inline JavaScript.

**Likely-agent-misses:**
- No package.json, build system, or standard frontend frameworks
- Everything is in ONE file: `index.html`
- No hot reload, bundling, or build process needed

## Entry Point
- `index.html` is the **only file to edit** - it contains HTML, CSS (Tailwind), and all JavaScript
- Open directly in browser to test, no server or build required

## Special Features to Know

### Secret Admin Mode
Click the **title "Ria & Ranto"** (3×) to show admin controls
- Located around line 262 in `index.html`
- Shows a floating gear icon (bottom-left corner)

### Guest Personalization
URL parameters to personalize the guest name:
- `?to=Andri%20Januardi%2C%20s.kom` - Sets guest name (see index.html:1273-1279)
- `?di=Banda%20Aceh%20/%20Tempat` - Sets guest location (see index.html:1281-1282)
- **Without parameters**: Shows "Tamu Kehormatan" (default text)

### Commented-Out Features
Major functionality is **disabled via HTML comments**:
- RSVP & wishes submission (entire section wrapped in `<!-- ... -->`)
- Admin dashboard operations
- Guest data management
- These sections exist but are commented out with no active code

### Empty API Calls
Admin features reference nonexistent PHP endpoints:
- `/add-guest.php`, `/add-wish.php`, `/delete-guest.php`, `/delete-wish.php`
- These URLs would 404 because no backend server exists

## JavaScript Scope
All interactive code is **embedded in `index.html`**:
- Smooth scroll sections
- Gallery lightbox
- Countdown timer
- Cover overlay animation
- URL parameter parsing (see index.html:1270-1287)
- No modular JavaScript architecture

## Testing & Iteration
Simply open `index.html` in any browser to test changes
- No test framework required
- No build commands to run
- Edit `index.html` and refresh browser

## What This **ISN'T**
- Not a React/Vue/Angular project
- No Node.js, npm, or build steps
- No TypeScript, no bundling, no linting
- No CI/CD, no deployment infrastructure
- No backend services, no database, no APIs

The **entire project lives in `index.html`** - edit that file and nothing else.
