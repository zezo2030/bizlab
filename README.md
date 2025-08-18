## BizLab – Digital Business Agency Landing Page

![BizLab preview](bizlab%20%282%29.png)

Modern, responsive landing page built with Tailwind CSS (via CDN) and minimal custom CSS.

### Features

- **Responsive header**: Desktop navigation and a mobile menu layout.
- **Hero section**: Full-width background image with dark overlay, headline, and dual CTAs.
- **About Us**: Image + content with two-column checklist of highlights.
- **CTA banner**: Centered call-to-action over a background image with overlay.
- **Services**: 6-card grid (Web Development, Graphic Design, Business Development, Digital Marketing, Web Hosting, Content Writing) with icons.
- **Split “Best Solution”**: Two-column section with image, description, and CTA button.
- **Stats**: 4 key metrics (Working Projects, Projects Done, Awards, Happy Clients) over an image background.
- **Pricing**: 3 pricing tiers (Basic, Standard, Corporate) with the middle plan visually featured.
- **Subscribe**: Newsletter email input with submit button.
- **Team**: 3 team member cards with avatars, roles, bios, and social links.
- **Footer**: Four columns (Products, Company, About, Social) + email subscribe in footer and copyright bar.
- **Back-to-top**: Floating action button to quickly return to the top.
- **Icons**: Iconify icon set for consistent, lightweight icons.

### Tech Stack

- **Tailwind CSS** via CDN: `@tailwindcss/browser@4`
- **Iconify** for icons
- **HTML5** and a small **custom CSS** overlay utility

### Project Structure

```txt
assets/
  css/
    style.css        # Overlay utility styles
  img/
    bg.jpg
    logo.png
    person.jpg
  js/                # (empty – no custom JS yet)
index.html           # Landing page markup
```

### How to Run

- Open `index.html` directly in your browser, or
- Serve the folder with a simple static server (recommended for correct asset paths):

```bash
# Option 1: Using Python (if installed)
python -m http.server 5500

# Option 2: Using Node (if installed)
npx serve . --listen 5500 --no-port-switching
```

Then visit `http://localhost:5500`.

### Customization

- **Branding**: Replace images in `assets/img/` (`logo.png`, `bg.jpg`, `person.jpg`).
- **Colors/Theme**: Tailwind utility classes are used throughout `index.html`. Update class names to change colors, spacing, and typography.
- **Icons**: Replace `data-icon` values on Iconify spans to change icons.
- **Overlay**: Tweak the overlay color/opacity in `assets/css/style.css`.
- **Content**: Edit headings, paragraphs, and list items directly in `index.html`.

### Notes

- The hero background uses Tailwind’s arbitrary value syntax: `bg-[url('/assets/img/bg.jpg')]`.
  - If you deploy under a sub-path, consider changing it to a relative path: `bg-[url('assets/img/bg.jpg')]`.
- The mobile menu markup is present, but there is no custom JS to toggle the `<dialog>` on small screens.
  - Add a small script to open the `#mobile-menu` dialog on burger click and close it on the close button.
- Forms (`Subscribe` and footer subscribe) are static and non-functional; wire them to your backend or a form service.

### License and Assets

This project is provided as a learning/demo template. Replace placeholder images and text with your own assets respecting their licenses.
