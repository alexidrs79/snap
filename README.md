# snap

Custom theme for **Snap**, an AI document-processing product for UK accounting. Built around ACF Pro field groups (one per landing-page section — Hero, Trust, Problem, Meet Snap, More Than OCR, Built for UK, How Snap Works, Real Usecases, CTA/Demo, Contact, Pricing) and template parts under `template-parts/`.

- Design source of truth: Figma file `Design Team — General` (node `15150-79`). Most section rules live in `style.css` and `template-parts/*.php`.
- Decorative icons/images live in the Media Library and are referenced from `inc/media-defaults.php` via `snap_print_icon()` (see `theme-setup.php`). Newer constants there hold a filename stem (e.g. `hero-scan-glyph`) rather than a numeric attachment ID — numeric IDs are environment-specific and silently break on any install other than the one they were captured against. Prefer the filename-stem style for anything new.
- Live site: `snaplanding.lucibook.co.uk`.

## Requirements

- WordPress 6.4 or newer, PHP 8.0 or newer
- Advanced Custom Fields **Pro** — field groups use repeaters and options pages, neither of which the free plugin provides, so a theme activated without it renders its sections empty.

## Installing

Copy or symlink this folder into `wp-content/themes/` and activate it. Create a page and assign the `Snap Landing` page template. Section content is then filled in on the page itself, with site-wide values under the theme's own options page.

## Deploys

There is no automated deploy. Code and content go live manually — a change that works locally is not live until it is copied up, and the database side (ACF values, Media Library items) has to be reproduced on the target install by hand.
