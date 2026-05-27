# DevArt Slider for Joomla

Professional slider builder for Joomla 6, designed for editorial, news, magazine, landing pages, and high-performance content-heavy websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.2%2B-green)
![Release](https://img.shields.io/badge/Version-1.0.0-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Slider is a modern Joomla 6 slider package built for stable frontend content presentation, high-traffic performance, video-enabled hero sections, editorial storytelling, and production-safe rendering.

It is designed for editorial, magazine, news, landing page, and enterprise Joomla websites that need a clean, secure, reliable, cache-friendly slider solution without unnecessary frontend bloat.

---

## Features

### Multiple Professional Templates

Includes 14 production-ready templates:

- Classic Hero
- Full Width Overlay
- Split Image / Text
- Multi Card Clean
- Multi Card Overlay
- Accordion Showcase
- Showcase Panels
- Hero Tiles
- Old Style Preview
- Classic News Sidebar
- Magazine Spotlight
- Overlay Box Hero
- Hover Editorial Cards
- Clean Fade Hero

Templates are designed for:

- editorial homepages
- featured content blocks
- landing pages
- magazine front pages
- storytelling sections
- promotional hero areas
- video showcase sections

---

### Flexible Content Sources

Supports multiple source modes:

- Latest Articles
- Featured Articles
- Selected Articles
- Custom Slides

Custom Slides support:

- title
- subtitle / intro
- badge
- date
- read more
- local image
- local MP4 / WEBM video
- poster image
- custom links

Perfect for:

- editorial stories
- breaking news
- campaigns
- marketing pages
- homepage hero sliders

---

### Video Support

Native video slide support:

- MP4 / WEBM local video
- poster image support
- autoplay support
- hover play / pause controls
- mobile-safe rendering
- lightweight frontend implementation

Designed without heavy third-party video dependencies.

---

### Joomla Frontend Module

Display sliders anywhere using Joomla module positions.

Features:

- slider selector
- Joomla native module integration
- access control support
- menu assignment support

Ideal for:

- homepage hero
- sidebar highlights
- category landing pages
- featured article blocks
- campaign pages

---

### Joomla Component Management

Manage sliders directly inside Joomla administrator.

Features:

- slider CRUD
- template selection
- typography controls
- theme presets
- transition settings
- autoplay controls
- arrows / dots controls
- height / ratio controls
- cache settings
- export / import workflow

---

### Theme Presets

Built-in theme presets:

- Red
- Blue
- Green
- Yellow
- Dark
- Light

Theme colors affect template accents consistently.

---

### Typography Controls

Global typography support:

- title size
- intro size
- badge styling
- date styling
- read more styling
- content color controls

Consistent across templates.

---

### Joomla Native Updates

DevArt Slider supports Joomla native updates via GitHub.

Once installed, future updates are available through:

`System → Extensions → Update`

Update server:

`https://raw.githubusercontent.com/devartgr/joomla-devart-slider/main/update.xml`

---

## Included Extensions

This package installs:

- com_devartslider
- mod_devartslider

---

## Requirements

- Joomla 6.x
- PHP 8.2+

---

## Installation

1. Download the latest release from GitHub
2. Go to:

`System → Extensions → Install`

3. Upload the package ZIP file
4. Open:

`Components → DevArt Slider`

5. Create your first slider
6. Publish the module where needed

---

## Performance

Built for production environments.

Features include:

- cache-first frontend rendering
- file-based frontend cache
- configurable cache duration
- minimal frontend JavaScript
- minimal CSS footprint
- safe query limits
- Joomla Page Cache friendly
- CDN friendly
- Cloudflare compatible
- high-traffic deployment friendly
- lightweight video rendering

Suitable for:

- editorial portals
- news websites
- magazine websites
- enterprise Joomla deployments

---

## Security Highlights

- Joomla ACL permissions support
- CSRF protection for administrator actions
- SQL injection protection through Joomla database APIs
- XSS-safe frontend rendering
- strict input validation
- protected cache directory structure
- safe Joomla native architecture
- GPL licensed
- JED-ready packaging

---

## Compatibility Notes

Supported:

- Joomla 6.x
- PHP 8.2+
- Joomla native update system
- modern Joomla MVC architecture

Not supported:

- Joomla 3
- Joomla 4
- Joomla 5
- legacy PHP versions

---

## Current Version

1.0.0

---

## Changelog 1.0.0

### Added

- Initial public production release
- Joomla 6 native component
- Joomla frontend module
- 14 professional slider templates
- article source modes
- custom slide source mode
- local image and video support
- hover video controls
- theme presets
- typography controls
- export / import support
- file-based frontend caching
- GitHub update server integration

### Improved

- cache-first frontend architecture
- high-traffic rendering strategy
- Cloudflare-friendly output
- mobile template behavior
- production-safe query limits
- isolated renderer architecture
- namespaced CSS / JavaScript

---

## Production Recommendations

Recommended defaults:

Frontend:

- enable caching
- enable autoplay where appropriate
- use optimized image sizes
- prefer poster images for video slides
- avoid excessive slide counts

Performance:

- cache duration: 15–60 minutes for news sites
- longer cache for static promotional sliders
- test Cloudflare cache behavior

Content:

- use Featured or Selected Articles for curated homepage blocks
- use Custom Slides for campaigns / marketing

---

## Known Notes

- Always test template compatibility and caching behavior before full production rollout
- Video-heavy sliders should be tested on mobile devices before deployment

---

## Author

Kostas Stathopoulos  
DevArt  
https://devart.gr/

GitHub Repository:

https://github.com/devartgr/joomla-devart-slider

---

## Disclaimer / Limitation of Liability

This software is provided "as is", without warranty of any kind.

DevArt shall not be held liable for any damages, data loss, downtime, security issues,
