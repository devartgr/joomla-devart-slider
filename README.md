# DevArt Slider for Joomla

Professional slider builder for Joomla 6, designed for editorial, news, magazine, landing pages, marketing campaigns, and high-performance content-heavy websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.2%2B-green)
![Release](https://img.shields.io/badge/Version-1.0.4-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Slider is a modern Joomla 6 slider package built for stable frontend content presentation, editorial storytelling, featured content promotion, video-enabled hero sections, and production-safe rendering.

Designed specifically for editorial, magazine, news, landing page, corporate, and enterprise Joomla websites, DevArt Slider focuses on performance, reliability, security, and maintainability while remaining fully compatible with Joomla 6 and modern PHP versions.

The package includes both a Joomla component and a Joomla frontend module for flexible deployment across any Joomla website.

---

## Features

### Professional Slider Templates

Includes multiple production-ready templates designed for different content presentation styles:

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
- Hover Overlay Cards
- Clean Fade Hero

Suitable for:

- Editorial homepages
- News portals
- Magazine front pages
- Landing pages
- Featured content blocks
- Marketing campaigns
- Product showcases
- Storytelling sections
- Video hero areas

---

### Flexible Content Sources

Supports multiple source modes:

- Latest Articles
- Featured Articles
- Selected Articles
- Custom Slides

Custom Slides support:

- Title
- Subtitle
- Intro text
- Badge label
- Date display
- Read More button
- Custom links
- Local images
- MP4 video
- WEBM video
- Poster images

Perfect for:

- Breaking news
- Featured stories
- Marketing campaigns
- Product launches
- Homepage hero areas
- Editorial promotions

---

### Native Video Support

Built-in video slide support without external dependencies.

Features:

- MP4 video support
- WEBM video support
- Poster image support
- Autoplay support
- Hover play/pause controls
- Mobile-friendly rendering
- Lightweight frontend implementation

---

### Joomla Frontend Module

Display sliders anywhere using Joomla module positions.

Features:

- Slider selector
- Joomla native module integration
- Menu assignment support
- Access control support
- Flexible positioning

Ideal for:

- Homepage heroes
- Sidebar highlights
- Landing pages
- Featured article areas
- Marketing campaigns

---

### Slider Management

Manage sliders directly through Joomla administrator.

Features:

- Slider CRUD
- Template selection
- Theme presets
- Typography controls
- Overlay controls
- Overlay style controls
- Autoplay settings
- Navigation controls
- Arrow controls
- Dot controls
- Height settings
- Ratio settings
- Cache settings
- Export support

---

### Global Overlay System

Built-in overlay engine shared across supported templates.

Overlay Styles:

- Uniform
- Bottom Focus
- Left Focus

Overlay Controls:

- Enable Overlay
- Overlay Color
- Overlay Opacity
- Overlay Style

Provides improved readability and editorial presentation without requiring template-specific overlay settings.

---

### Theme Presets

Built-in theme presets:

- Red
- Blue
- Green
- Yellow
- Dark
- Light

Themes provide consistent styling across supported templates.

---

### Typography Controls

Global typography management:

- Title size
- Intro size
- Badge styling
- Date styling
- Read More styling
- Content color controls

Provides consistent presentation across templates.

---

### Advanced Image Handling

Image rendering is designed for performance-oriented websites.

Features:

- Original Image mode
- Cached Resize mode
- Cached Crop mode
- Dedicated cached image dimensions
- Independent slider dimensions
- Automatic thumbnail generation
- Automatic thumbnail retention management
- Manual image cache cleanup tools

Benefits:

- Reduced bandwidth usage
- Faster frontend rendering
- Improved cache efficiency
- Better support for card-based templates
- Improved performance on high-traffic websites

---

### Intelligent Thumbnail Cache

DevArt Slider includes a dedicated thumbnail cache system.

Features:

- File-based thumbnail cache
- Cached image generation
- Configurable thumbnail retention period
- Automatic expired thumbnail cleanup
- Manual image cache cleanup
- Cloudflare-friendly architecture

Designed specifically for editorial websites that continuously publish new content and images.

---

### Joomla Native Updates

Supports Joomla native updates via GitHub.

After installation future releases can be installed through:

System → Extensions → Update

Update Server:

https://raw.githubusercontent.com/devartgr/joomla-devart-slider/main/update.xml

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

1. Download the latest release package
2. Open:

   System → Extensions → Install

3. Upload the ZIP package
4. Open:

   Components → DevArt Slider

5. Create a slider
6. Publish the module where required

---

## Performance

Built for production environments.

Features include:

- Cache-first frontend rendering
- File-based frontend cache
- Dedicated thumbnail cache
- Configurable cache duration
- Configurable thumbnail retention
- Minimal frontend JavaScript
- Lightweight CSS architecture
- Safe query limits
- Joomla Page Cache friendly
- CDN friendly
- Cloudflare compatible
- High-traffic deployment friendly

Suitable for:

- News portals
- Editorial websites
- Magazine websites
- Enterprise Joomla deployments
- High-volume content websites

---

## Security Highlights

- Joomla ACL permissions support
- CSRF protection for administrator actions
- SQL injection protection through Joomla database APIs
- XSS-safe frontend rendering
- Strict input validation
- Protected cache directory structure
- Secure Joomla native architecture
- GPL licensed
- JED-ready packaging

---

## Compatibility

Supported:

- Joomla 6.x
- PHP 8.2+
- Joomla native update system
- Modern Joomla MVC architecture

Not Supported:

- Joomla 3
- Joomla 4
- Joomla 5
- Legacy PHP versions

---

## Current Version

1.0.4

---

## What's New in 1.0.4

### Added

- Global Overlay Style system
- Uniform overlay mode
- Bottom Focus overlay mode
- Left Focus overlay mode
- Image shadow support for Split Image / Text Slider
- Overlay content mode for Classic News Sidebar
- Theme-colored active preview highlighting
- Improved editorial thumbnail presentation for Magazine Spotlight

### Fixed

- Overlay rendering inconsistencies across templates
- Overlay disable behavior in affected templates
- Navigation positioning issues in preview-based templates
- Dots and arrows rendering issues in multiple templates
- Template configuration inconsistencies
- Language string display issues in template settings

### Improved

- Split Image / Text Slider layout and navigation
- Full Width Overlay rendering behavior
- Old Style Preview navigation controls
- Classic News Sidebar preview rendering
- Magazine Spotlight editorial presentation
- Overlay flexibility for editorial websites
- Template-specific settings visibility
- Administrator usability and configuration consistency

### Removed

- Unused Image Dark Overlay setting from Clean Fade Hero
- Unused Transition Effect setting from Hover Overlay Cards
- Unused Transition Speed setting from Hover Overlay Cards

---

## Production Recommendations

Recommended settings for news and editorial websites:

### Frontend

- Enable caching
- Use Cached Resize images
- Use optimized image dimensions
- Limit excessive slide counts
- Use poster images for video slides

### Cache

- Slider cache: 15–60 minutes
- Thumbnail retention: 7–30 days
- Use manual cache clearing only when required

### Content

- Use Featured Articles for homepage highlights
- Use Selected Articles for curated content
- Use Custom Slides for campaigns and promotions

---

## Author

Kostas Stathopoulos  
DevArt  
https://devart.gr

GitHub Repository:

https://github.com/devartgr/joomla-devart-slider

---

## License

GNU General Public License v3.0 (GPLv3)

---

## Disclaimer / Limitation of Liability

This software is provided "as is", without warranty of any kind.

DevArt shall not be held liable for any damages, data loss, downtime, security incidents, business interruption, loss of profits, or other consequences arising from the use or inability to use this software.

Always test updates in a staging environment before deploying to production systems.
