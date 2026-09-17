# Coffee Corner — Lomé

Showcase website for Coffee Corner, a coffee shop in Lomé, Togo. A single-page static
site built with plain HTML, CSS and JavaScript — no framework, no build step, no
dependencies beyond Google Fonts.

The page content is written in French, since that's the language of the shop's customers.

## Sections

| Section | Anchor | Content |
|---------|--------|---------|
| Hero | `#accueil` | Tagline and calls to action towards the menu and the contact details |
| About | `#apropos` | The shop's story and its selling points (locally roasted beans, pastries made each morning, free wifi) |
| Menu | `#menu` | Six cards — espresso, cappuccino, iced coffee, hot chocolate, croissant, slice of cake — with prices in FCFA |
| Reviews | `#avis` | Three customer testimonials |
| Contact | `#contact` | Address, phone, email, opening hours and a contact form |

## Features

- Responsive layout with a burger menu on small screens that closes itself when a link
is clicked
- Smooth anchor navigation between sections
- Footer year filled in automatically from `new Date().getFullYear()`
- Contact form with a confirmation message
- Typography: [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) for
headings, [Poppins](https://fonts.google.com/specimen/Poppins) for body text

## Project structure

```
Coffe_website/
├── index.html   # all the page content
├── style.css    # styles, layout, responsive breakpoints
└── script.js    # burger menu, footer year, contact form handling
```

## Running it locally

Nothing to install — open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

## Before going live

A few things in this version are placeholders and need replacing with the real details:

- **The contact form has no backend.** `script.js` calls `preventDefault()`, clears the
fields and shows a thank-you message — nothing is sent or stored anywhere. Wire it up to
a form service (Formspree, Netlify Forms, EmailJS...) or your own endpoint before
advertising it.
- **Contact details are placeholders**: the phone number (`+228 90 00 00 00`), the email
address and the street address in `index.html` all need to be filled in with the shop's
real information.
- Menu items and prices should be checked against the current menu.

## Deployment

Being a purely static site, it can be published as is on GitHub Pages, Netlify, Vercel,
or any classic web host — just upload the three files.
