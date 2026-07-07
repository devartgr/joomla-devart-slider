# DevArt Slider for Joomla

Professional slider builder for Joomla 6, designed for editorial, news, magazine, landing pages, marketing campaigns, business directories, event websites, video portals, and high-performance content-heavy websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.2%2B-green)
![Release](https://img.shields.io/badge/Version-1.0.7-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Slider is a modern Joomla 6 slider package built for stable frontend content presentation, editorial storytelling, featured content promotion, video-enabled hero sections, and production-safe rendering.

Designed specifically for editorial, magazine, news, landing page, corporate, business directory, event, video, and enterprise Joomla websites, DevArt Slider focuses on performance, reliability, security, and maintainability while remaining fully compatible with Joomla 6 and modern PHP versions.

The package includes both a Joomla component and a Joomla frontend module for flexible deployment across any Joomla website.

---

## Features

### Professional Slider Templates

Includes multiple production-ready templates designed for different content presentation styles.

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
- Business directories
- Event websites
- Video portals
- Storytelling sections
- Video hero areas

---

## Flexible Content Sources

Supports multiple native source providers through a unified rendering engine.

### Joomla Articles

- Latest Articles
- Featured Articles
- Selected Articles

### DevArt Business

- All Categories
- Selected Categories
- Include Child Categories
- Featured Handling

### DevArt Events

- All Categories
- Selected Categories
- Include Child Categories
- Event Time filtering
  - Today
  - Upcoming
  - Past
  - All
- Featured Handling

Events use the same event date logic as the DevArt Events component, ensuring consistent results across the frontend, modules, and slider.

### DevArt Video

- All Categories
- Selected Categories
- Include Child Categories
- Featured Handling
- Newest
- Oldest

Video content is rendered using the same lightweight rendering engine, image pipeline, and caching architecture as every other supported content source.

### Custom Slides

Supports:

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

The slider architecture is designed to support multiple native DevArt content providers while preserving one common rendering pipeline and template system.

---

## Native Video Support

Built-in video support without external dependencies.

Features:

- MP4 video
- WEBM video
- Poster images
- Autoplay
- Hover play / pause
- Mobile-friendly rendering
- Lightweight frontend implementation

---

## Joomla Frontend Module

Display sliders anywhere using Joomla module positions.

Features:

- Slider selector
- Joomla native module integration
- Menu assignment
- Access control
- Flexible positioning

Ideal for:

- Homepage heroes
- Sidebar highlights
- Landing pages
- Featured article areas
- Featured businesses
- Featured events
- Featured videos
- Marketing campaigns

---

## Slider Management

Manage sliders directly through Joomla Administrator.

Features:

- Slider CRUD
- Multiple content sources
- Template selection
- Theme presets
- Typography controls
- Overlay controls
- Overlay styles
- Autoplay
- Navigation
- Arrows
- Dots
- Height controls
- Cache controls
- Export support

---

## Global Overlay System

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

---

## Theme Presets

Built-in presets:

- Red
- Blue
- Green
- Yellow
- Dark
- Light

---

## Typography Controls

Global typography management.

- Title size
- Intro size
- Badge styling
- Date styling
- Read More styling
- Content colors

---

## Advanced Image Handling

Image rendering is designed for high-performance websites.

Features:

- Original Image
- Cached Resize
- Cached Crop
- Dedicated cache dimensions
- Automatic thumbnail generation
- Automatic cleanup
- Configurable retention period
- Manual cache clearing

Benefits:

- Lower bandwidth usage
- Faster rendering
- Better cache efficiency
- Production-ready performance

---

## Intelligent Cache Architecture

Features:

- File-based frontend cache
- Intelligent thumbnail cache
- Automatic cleanup
- Cloudflare compatible
- CDN friendly
- Shared rendering pipeline across all content providers

---

## Joomla Native Updates

Supports Joomla native updates through GitHub.

**System → Extensions → Update**

---

## Included Extensions

- com_devartslider
- mod_devartslider

---

## Requirements

- Joomla 6.x
- PHP 8.2+

---

## Installation

1. Install the package.
2. Open **Components → DevArt Slider**.
3. Create a slider.
4. Select a content source.
5. Publish the module.

---

## Performance

Built for production websites.

Features include:

- Cache-first rendering
- File-based frontend cache
- Thumbnail cache
- Cloudflare compatible
- CDN friendly
- Lightweight frontend assets
- Optimized database queries
- High-traffic ready

Suitable for:

- News portals
- Editorial websites
- Magazine websites
- Business directories
- Event websites
- Video portals
- Enterprise Joomla deployments

---

## Security Highlights

- Joomla ACL support
- CSRF protection
- SQL injection protection
- XSS-safe rendering
- Strict input validation
- Protected cache directories
- Modern Joomla architecture

---

## Compatibility

Supported:

- Joomla 6.x
- PHP 8.2+
- Joomla native updates
- Modern Joomla MVC

Not Supported:

- Joomla 3
- Joomla 4
- Joomla 5
- Legacy PHP

---

## Current Version

**1.0.7**

---

## What's New in 1.0.7

### Added

- Native DevArt Video source support
- Video category filtering
- Include Child Categories for videos
- Featured Handling for videos
- Video ordering (Newest / Oldest)

### Improved

- Extended the native multi-source architecture with DevArt Video integration
- Unified configuration across Articles, Business, Events and Video sources
- Shared rendering, image handling and cache pipeline for Video content
- Improved provider compatibility and frontend consistency

### Fixed

- Video provider integration improvements
- Video category filtering improvements
- Featured video handling improvements
- Video query stability improvements
- General stability and compatibility improvements

### Notes

- No database schema changes
- No template changes
- Existing sliders remain fully compatible
- Safe update from all previous 1.0.x releases
- Recommended for installations using DevArt Video

---

## Production Recommendations

### Frontend

- Enable caching
- Use Cached Resize images
- Optimize image dimensions
- Keep slide counts reasonable

### Content

- Use Featured Articles for editorial highlights
- Use DevArt Business for directory showcases
- Use DevArt Events for upcoming events
- Use DevArt Video for featured video sections
- Use Custom Slides for campaigns and promotions

---

## Author

Kostas Stathopoulos

DevArt

https://devart.gr

GitHub

https://github.com/devartgr/joomla-devart-slider

---

## License

GNU General Public License v3.0 (GPLv3)

---

## Disclaimer

This software is provided "as is", without warranty of any kind.

Always test updates in a staging environment before deploying to production.
