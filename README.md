Greenden Clone
A clean, responsive clone of the Greenden landing and store experience built with HTML, Tailwind CSS (CDN), and minimal vanilla JavaScript. It includes a homepage, products page with quick‑view modal and filters, and a contact page with a working responsive navbar.

Demo

Live Demo: add-your-deploy-url-here
Repository: add-your-repo-url-here
Screenshots

Home: docs/screenshots/home.png
Products: docs/screenshots/products.png
Contact: docs/screenshots/contact.png
Tech Stack

HTML5
Tailwind CSS (CDN)
Vanilla JavaScript (no frameworks)
Features

Fully responsive layout (mobile-first)
Sticky navbar with mobile hamburger menu
“Shop Now” button linking to Products page
“Watch Video” modal (YouTube embed)
Products page with:
Category filter tabs (All, Indoor, Outdoor, Succulents, Flowering)
Search box (client-side filter by name)
Quick-view modal (click any product to see details)
Accessible interactions:
Esc closes modals
Overlay click closes modals
Focus-visible rings on interactive elements
Performance-friendly:
Lazy-loaded images
Lightweight JS and Tailwind via CDN
Project Structure

index.html Home page (hero, about, best sellers, reviews, newsletter)
products.html Full products grid + filters + quick-view modal
contact.html Contact form + responsive navbar
images/ Local image assets (add your plant images here)
docs/screenshots/ Optional screenshots for README
Getting Started

Clone the repo
git clone https://github.com/your-username/greenden-clone.git
cd greenden-clone
2. Open locally

Double-click index.html to open in your browser, or
Use a local server (recommended for better routing):
VS Code extension “Live Server” → right click index.html → Open with Live Server
No build step is required because Tailwind is loaded from the CDN.

Pages Overview

index.html

Hero with “Shop Now” (links to products.html) and “Watch Video” (opens modal)
About section
Best Sellers preview
Customer reviews
Newsletter
products.html

Filter tabs (All/Indoor/Outdoor/Succulents/Flowering)
Search input (filters by product name)
12+ product cards (mix of local and Unsplash images)
Quick View modal when clicking a card
contact.html

Simple, accessible contact form
Reuses the same responsive navbar
Linking Shop and Watch Video
Option A: Link buttons directly (no JS)

Shop Now: <a href="products.html" class="bg-black text-white px-4 py-2 rounded">Shop Now</a>
Watch Video (to a YouTube page in a new tab): <a href="https://www.youtube.com/watch?v=M7lc1UVf-VE" target="_blank" class="border px-4 py-2 rounded">Watch Video</a>
Option B: Use the built-in video modal

The provided index.html already includes a small video modal.
To use your own video, replace the YouTube ID in the JS: openV('YOUR_VIDEO_ID_HERE')
Customize Products

Add/replace images in images/
In products.html, duplicate any “product” card div: <div class="product" data-cat="indoor" data-name="New Plant" data-price="$29"> <img src="./images/your-image.jpg" alt="New Plant" loading="lazy" class="w-full rounded"> <h3 class="font-semibold mt-1">New Plant</h3><p>$29</p> </div>
Update data-cat values so filters work:
indoor, outdoor, succulent, flowering
Update data-name (for search) and data-price.
Accessibility Notes

Focus states are visible on buttons/links
Esc key and overlay close all modals
alt text is present on images
Buttons have aria-labels where icons are used
Performance Tips

Use local, optimized images in images/
Keep Unsplash images if you want quick variety, but local images load faster offline
Tailwind via CDN keeps setup simple; if you need production purging, switch to Tailwind CLI
