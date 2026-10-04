# Riva (ريڤا) — Coworking Space Landing Page

A single-page, right-to-left Arabic landing page for Riva, a coworking space offering shared desks, private offices and meeting rooms in Sharqia, Egypt.

The whole site is one file, [index.html](index.html). There is no build step.

## Run it

Open `index.html` in a browser, or serve the folder with any static server:

```
npx serve .
```

An internet connection is needed, because Tailwind, the fonts and the images are loaded from external URLs.

## What's on the page

1. Sticky header with navigation (collapses to a menu button below 1024px)
2. Hero with opening hours and booking buttons
3. Three offerings: shared workspace, private offices, meeting rooms
4. Facilities
5. Pricing: morning and evening packages
6. Solutions for companies
7. Photo gallery
8. Testimonials
9. FAQ
10. Final call to action with contact details
11. Footer

Every booking button opens a WhatsApp chat with a pre-filled message.

## Tech

- Plain HTML with [Tailwind CSS](https://tailwindcss.com) loaded from the Play CDN; the theme (colors, fonts) is configured in a `<script>` block in the `<head>`
- Google Fonts: Alexandria for headings, IBM Plex Sans Arabic for body text
- A few lines of vanilla JavaScript for the mobile menu

## Before going live

The page still contains placeholder content that must be replaced:

| What | Current value | Where |
| --- | --- | --- |
| WhatsApp number | `201000000000` | every `wa.me` link |
| Phone number | `+20 1XX XXX XXXX` / `tel:+201000000000` | final call-to-action section |
| Address | `[العنوان بالتفصيل]` | final call-to-action section |
| Map link | `https://maps.google.com` | final call-to-action section |
| Images | hotlinked from `lh3.googleusercontent.com` | all `<img>` tags |

Two more things to do for production:

- **Host the images yourself.** The current image URLs are not permanent and may stop working.
- **Replace the Tailwind Play CDN.** It is intended for development only; generate a compiled CSS file with the Tailwind CLI instead.
