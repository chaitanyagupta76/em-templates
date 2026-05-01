As a creative website UI designer create a wedding website mock image with the following sections. Use the images attached as references.
 1. Hero section with multiple candles . Couple name and date and right side couple slide show in frame. 
 2. Brdie groom section. With photos of couple name in elgant border, and parents name names.
 3. Venue and recption section with map a. Elegant border with leafs attached in this 
 4. Timeline of events. Photos,date and descritpion 
 5. Live stgream section with a video 
 6. Gallery section with photos in mosiac pattern 
 7. Waiting presence with parents photos of both bride and groom and waiting presence text.

 ==========================================
 🔶 Prompt: Wedding Website (Next.js + Tailwind + Flatfile-driven + i18n)

Design and develop a fully responsive wedding website inspired by an elegant Indian wedding theme using Next.js (App Router) and Tailwind CSS.

🔶 Core Requirements
1. Architecture
Use Next.js (latest, App Router)
Use Tailwind CSS for styling
Follow component-driven architecture
Ensure mobile-first responsive design
Use dynamic imports and lazy loading for performance
2. Data Handling (Flatfile-based CMS)

All dynamic content must be loaded from flat files (JSON/YAML):

📁 Structure:
/data
  /en.json
  /te.json
  /config.json
  /gallery.json
  /events.json
Rules:
All text content → loaded from translation files (en.json, te.json)
Images (except UI decorative assets) → loaded from flatfile JSON or external URLs
Config-driven sections → enable/disable sections via config.json
3. Internationalization (i18n)
Support English (default) and Telugu
Language switcher toggle in header
Translations should:
Load from local JSON files
Also support remote loading via URL (API or CDN)

Example:

fetch('/data/en.json')
// OR
fetch('https://cdn.example.com/translations/en.json')
4. UI Design Theme
Color palette: ivory, gold, soft beige
Use ornamental borders and floral elements (like provided images)
Typography:
Elegant serif for headings
Clean sans-serif for body
Use subtle animations (fade, slide, parallax)
🔶 Sections to Implement
1. Hero Section
Background with multiple glowing candles
Center:
Couple names
Wedding date
Right side:
Image slideshow inside ornate frame
Add soft animation (floating glow / fade)
2. Bride & Groom Section
Two columns:
Bride
Groom
Each includes:
Photo
Name inside decorative border
Parents’ names
Use elegant floral dividers
3. Venue & Reception Section
Card layout with:
Venue image
Embedded Google Map iframe
Address text
Surround with leaf + floral borders
Add CTA: “View Directions”
4. Timeline of Events
Vertical timeline
Each event card includes:
Photo
Title
Date & time
Description
Alternating left-right layout (desktop)
Single column (mobile)
5. Live Stream Section
Embedded video player (YouTube / custom URL)
Styled container with decorative frame
Optional: “Join Live” button
6. Gallery Section
Mosaic / masonry grid layout
Images loaded from flatfile (gallery.json)
Lightbox preview on click
7. Wedding Presence Section
Display:
Bride’s parents
Groom’s parents
Include photos + names
Add heading:
“We request the honor of your presence”
Elegant centered layout
🔶 Config-Driven Sections

Example config.json:

{
  "hero": true,
  "brideGroom": true,
  "venue": true,
  "timeline": true,
  "livestream": true,
  "gallery": true,
  "presence": true
}

Each section must render conditionally.

🔶 Performance & UX
Use:
next/image for optimization
Lazy loading for gallery & slideshow
Ensure:
Fast load (<2s ideal)
Smooth scrolling
Accessibility (ARIA labels)
🔶 Folder Structure
/app
/components
  Hero.tsx
  BrideGroom.tsx
  Venue.tsx
  Timeline.tsx
  LiveStream.tsx
  Gallery.tsx
  Presence.tsx
/lib
  i18n.ts
  fetchData.ts
/data
/public/assets (UI decorative images only)
🔶 Bonus Enhancements (Optional but Recommended)
Background music toggle 🎵
RSVP form (store in API / sheet)
Countdown timer
WhatsApp share button
🔶 Output Expectation
Clean, modular code
Fully responsive across:
Mobile
Tablet
Desktop
Easily configurable via flatfiles
Ready for deployment (Vercel preferred)