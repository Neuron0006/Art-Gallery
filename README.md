# ArtSpace — Member Photo Access + CSS Magnifier

A responsive art gallery prototype made with **HTML and CSS only**. It contains no JavaScript, no JavaScript libraries, and no backend.

## New features in this edition

- `login.html` — a styled member login portal. The “Preview member access” control is a CSS checkbox demonstration; it reveals the sample photo-library link.
- `downloads.html` — a photo library with magnifier links and source/download links for each sample image.
- `photo-viewer.html` — a CSS-only image viewer. Click a photo card, then choose Fit, 150%, or 200%. At higher zoom levels, scroll inside the image frame.
- The homepage and creator profile now use online Unsplash images instead of gradient-only artwork cards.

## Important: the login is not real authentication

This project is intentionally limited to HTML and CSS. The login page does **not** verify email addresses or passwords, does not create a session, and does not send or store credentials. The checkbox simply reveals a demo link. Anyone can open `downloads.html` directly or inspect the source. Do not enter a real password.

A real access-controlled download area requires server-side authentication and authorization. Hiding a link with CSS is not a security boundary.

## Important: photo download behaviour

The sample photographs are loaded from Unsplash's image CDN and are not stored inside this ZIP. An internet connection is required to display them. “Download source” opens the photographer's Unsplash photo page, where the visitor can use its Download option. “Open full-size image” opens the image directly; visitors can use their browser's Save image option. Browsers generally ignore the HTML `download` attribute for cross-origin image URLs, so these links deliberately open the source rather than pretending to force a download.

## CSS-only magnifier

The viewer uses URL fragments (`:target`) to choose the photo and radio inputs with CSS `:checked` / `:has()` selectors to change the image width to 100%, 150%, or 200%. No scripts are used.

## Main files

- `index.html` — homepage, gallery and category filters
- `artwork.html` — example artwork detail page
- `creator.html` — creator profile and portfolio
- `studio.html` — creator dashboard and form UI
- `admin.html` — moderation dashboard UI
- `login.html` — demo member-access screen
- `downloads.html` — photo download/source library
- `photo-viewer.html` — CSS magnifier
- `styles.css` — shared styling, responsive layout and CSS animations

## Run it

1. Extract the ZIP.
2. Open the `artspace-member-downloads` folder in VS Code.
3. Open `index.html` in Chrome, or use VS Code's Live Server extension.
4. Choose “Member login” in the navigation, then click “Preview member access”.
5. Open a photo in the library and test Fit / 150% / 200% zoom.

## Sample photo credits

Each source page identifies the image as free to use under the Unsplash License at the time checked. Please recheck the license and source details before using these images in a public or commercial release.

- Abstract painting — CHUTTERSNAP: https://unsplash.com/photos/abstract-painting-uj1tRjP5UI0
- Ocean waves — Alexa: https://unsplash.com/photos/ocean-waves-G1RBwD_wchw
- Flower close-up — Anton Murygin: https://unsplash.com/photos/closeup-photography-of-flowers-q-HbOPtFfaM
- Sculptural digital artwork — Khyati Trehan / Visualising AI: https://unsplash.com/photos/a-close-up-of-a-sculpture-rXy5Zlmw3qY
- Aerial river landscape — Jonatan Pie: https://unsplash.com/photos/a-winding-river-flows-through-a-vast-dark-landscape-Y19Sstu3_DI
- White sculptures in a gallery — Kinsey Wang: https://unsplash.com/photos/abstract-white-sculptures-in-dim-room-74jrYJkUxzE
- Artist working in studio — Vitaly Gariev: https://unsplash.com/photos/artist-painting-on-canvas-in-a-studio-setting-1QAJymq9rB4

## Feature limitations

Category filters, CSS animations, the demo access reveal, and the image magnifier work in modern browsers. The login, protected downloads, database, saved favourites, search, uploads, publishing, editing, deleting, and admin moderation remain front-end demonstrations only.
