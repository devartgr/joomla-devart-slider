# DevArt Slider for Joomla

Professional multi-source slider solution for Joomla 6, designed for news portals, magazines, publishers, municipalities, organizations, business websites, agencies, and high-traffic production environments.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.3%2B-green)
![Release](https://img.shields.io/badge/Version-1.0.8-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Slider is a modern Joomla 6 slider component and module built for creating responsive, professional content sliders from multiple Joomla and DevArt content sources.

The extension is designed for production websites where performance, stability, responsive rendering, and administrator usability are essential.

DevArt Slider supports Joomla Articles, manually created slides, DevArt Business, DevArt Events, and DevArt Video through a unified multi-source architecture.

It includes multiple production-ready templates, configurable themes, image processing, frontend caching, responsive controls, and a high-performance Joomla-style article selector designed to remain usable even on websites containing hundreds of thousands of articles.

---

## Large Website Performance

DevArt Slider is designed to work safely on both small websites and very large Joomla installations.

The extension avoids loading complete article collections into administrator forms and does not preload the entire Joomla content table when selecting articles.

The Selected Articles workflow uses a bounded Joomla-style modal selector with:

- Server-side article browsing
- Fast article search
- Bounded result sets
- Controlled pagination
- Multi-page article selection
- Two-phase article loading
- No full article table preload
- No unbounded administrator article queries
- No requirement to increase the PHP memory limit

The article selector has been successfully tested on a production-scale Joomla environment containing more than **220,000 Joomla Articles**.

In this environment:

- The selector modal opened in milliseconds
- Article search remained fast
- Pagination remained responsive
- Multiple article selection worked normally
- No PHP memory exhaustion occurred
- No administrator timeout occurred
- No Cloudflare timeout occurred
- Existing selected article configurations remained compatible

This architecture makes DevArt Slider suitable for large editorial websites, news portals, archives, publishers, and other Joomla installations with very large content databases.

---

## Package Contents

The installable package includes:

- `com_devartslider` — Slider management component
- `mod_devartslider` — Frontend slider module

The complete package can be installed or updated directly through the standard Joomla Extensions installer.

---

## Content Sources

DevArt Slider supports multiple content sources through a unified rendering system.

### Joomla Articles

Create sliders from Joomla Articles using:

- Latest Articles
- Featured Articles
- Selected Articles
- Category filtering
- Child category inclusion
- Featured handling
- Configurable ordering
- Article limits and skip values

### Selected Articles

The Selected Articles source includes a high-performance Joomla administrator modal with:

- Search by article title
- Exact article ID search
- Server-side pagination
- Multi-page selection
- Persistent selections while browsing
- Add Selected workflow
- Done action for adding selections and closing the modal
- Selected article removal
- Selected article reordering
- Preservation of existing article IDs and order

The selector stores article IDs using the existing DevArt Slider configuration format and remains compatible with previously created sliders.

### Custom Slides

Create manually managed slides with custom:

- Titles
- Text
- Images
- Links
- Buttons
- Video content
- Ordering

### DevArt Business

Create sliders from DevArt Business listings with:

- All Categories or Selected Categories
- Child category inclusion
- Featured business handling
- Configurable ordering
- Existing slider image and cache pipeline

DevArt Business integration is optional and becomes available when the corresponding extension is installed.

### DevArt Events

Create sliders from DevArt Events with:

- Today
- Upcoming
- Past
- All Events
- Category filtering
- Child category inclusion
- Featured event handling
- Event occurrence-aware ordering

Event selection uses the actual DevArt Events date information instead of Joomla article publishing dates.

DevArt Events integration is optional.

### DevArt Video

Create sliders from DevArt Video with:

- All Categories or Selected Categories
- Child category inclusion
- Featured video handling
- Newest or Oldest ordering
- Existing slider image, rendering, and cache pipeline

DevArt Video integration is optional.

---

## Slider Templates

DevArt Slider includes multiple responsive, production-ready templates for different website styles and content types.

Available designs include editorial, magazine, news, card, preview, overlay, hero, sidebar, and split-content layouts.

Template capabilities include:

- Responsive slide layouts
- Full-width presentation
- Thumbnail navigation
- Preview navigation
- Magazine-style presentation
- News sidebar presentation
- Split image and text layouts
- Overlay content
- Hover controls
- Dots and arrows
- Active slide highlighting
- Configurable transitions
- Mobile-optimized behavior

Template-specific settings are displayed only where they are relevant.

---

## Themes

Built-in theme options allow sliders to match different website designs without custom code.

Available theme families include:

- Red
- Orange
- Blue
- Green
- Yellow
- Gray
- Dark
- Light

Theme settings are applied consistently across supported templates, navigation controls, active states, buttons, and preview elements.

---

## Overlay System

DevArt Slider includes flexible overlay presentation options such as:

- Uniform
- Bottom Focus
- Left Focus

Overlay settings can be used with supported templates to improve text readability and create editorial, magazine, or promotional layouts.

---

## Image Handling

DevArt Slider includes a production-oriented image processing system with:

- Configurable display dimensions
- Separate cached image dimensions
- Automatic thumbnail generation
- Cached thumbnail storage
- Configurable thumbnail retention
- Automatic cleanup of expired thumbnails
- Manual image cache clearing
- Responsive image presentation
- Template-specific image handling

Image cache cleanup is controlled and does not run during the high-performance article selection modal request.

---

## Video Slides

Supported templates can display video-based slides with lightweight frontend controls.

Video capabilities include:

- Video slide rendering
- Play and pause controls
- Hover interaction
- Existing responsive slider pipeline
- Integration with DevArt Video content sources

---

## Frontend Performance

DevArt Slider uses a cache-first frontend architecture intended for production and high-traffic websites.

Performance characteristics include:

- File-based frontend cache
- Configurable cache duration
- Controlled database queries
- Bounded source result limits
- Cached image processing
- Reuse of normalized slider items
- Lightweight frontend JavaScript
- No jQuery dependency
- Namespaced CSS and JavaScript
- Cloudflare-friendly frontend rendering
- CDN-compatible static assets
- Stable rendering under high traffic

The component avoids unnecessary work during cached frontend requests and uses the same rendering pipeline across supported content sources.

---

## Administrator Performance

The administrator interface is designed to remain responsive when working with large databases.

Important safeguards include:

- No full Joomla Article table preload
- No enormous HTML article dropdown
- No unbounded Article SQL form field
- Bounded article selector result sets
- Controlled page size
- Server-side search and pagination
- Direct loading of only required selected article IDs
- Preservation of unavailable stored IDs without scanning the full content table
- No exact full-table count requirement in the article selector
- Safe Joomla MVC state handling

These safeguards prevent the memory exhaustion and timeout problems commonly caused by loading thousands or hundreds of thousands of articles into a standard select field.

---

## Caching

DevArt Slider includes configurable frontend caching to reduce repeated database and rendering work.

Cache features include:

- File-based slider output cache
- Configurable cache lifetime
- Cache separation by slider configuration
- Administrator cache clearing
- Safe handling of empty source results
- Cached thumbnail management
- Compatibility with reverse proxies and CDN environments

Joomla module caching options can also be used according to the website configuration.

---

## Responsive Design

All slider templates are designed for responsive frontend presentation.

Responsive behavior includes:

- Desktop layouts
- Tablet layouts
- Mobile layouts
- Responsive images
- Adaptive navigation
- Touch-friendly controls
- Mobile-specific template behavior
- Controlled text and overlay presentation

---

## Accessibility

DevArt Slider uses semantic controls and accessible frontend interaction wherever supported by the selected template.

Accessibility-related features include:

- Button elements for interactive controls
- Keyboard-compatible actions
- Accessible modal controls
- Visible focus behavior
- Descriptive navigation labels
- Proper image alternative text handling
- Administrator controls compatible with Joomla Atum conventions

---

## Joomla-Native Architecture

DevArt Slider follows modern Joomla development patterns, including:

- Joomla 6 MVC architecture
- Namespaced PHP classes
- Joomla service provider architecture
- Joomla Web Asset Manager
- Joomla Form API
- Joomla ACL
- Joomla database APIs
- Joomla administrator layouts
- JoomlaDialog modal integration
- SearchTools-compatible administrator interface
- CSRF protection
- Proper input filtering
- Escaped output

No Joomla legacy compatibility layer is included.

---

## Security

Security measures include:

- Joomla ACL enforcement
- CSRF protection for administrator actions
- Input filtering and normalization
- Integer normalization for selected IDs
- Joomla database query APIs
- Parameterized or safely constructed queries
- Output escaping
- Same-origin modal communication checks
- Controlled administrator-only article selection
- No exposure of SQL errors or server paths in normal operation
- Protected cache directories
- Safe package installation and update handling

---

## Permissions

DevArt Slider integrates with Joomla ACL.

Administrators can configure permissions for actions such as:

- Accessing the component
- Creating sliders
- Editing sliders
- Changing state
- Deleting sliders
- Managing component options

Permission behavior follows Joomla user groups and viewing access conventions.

---

## Import and Export

Slider configurations can be exported for backup or transfer purposes.

Existing Selected Articles data remains compatible with the new modal selector because the stored format is unchanged.

Selected article IDs continue to be stored as an ordered integer list within the slider configuration.

---

## Requirements

- Joomla 6.x
- PHP 8.3 or newer
- MySQL or MariaDB supported by Joomla 6
- PHP GD or other required image support according to the Joomla server configuration
- A modern browser for administrator and frontend interfaces

Optional integrations require the corresponding DevArt extension:

- DevArt Business
- DevArt Events
- DevArt Video

---

## Installation

1. Download the latest package: `pkg_devartslider_v1.0.8.zip`
2. Open the Joomla administrator.
3. Go to `System → Install → Extensions`.
4. Upload and install the package.
5. Open `Components → DevArt Slider`.
6. Create a slider.
7. Publish a DevArt Slider module and select the required slider.

The package supports Joomla update installation over previous DevArt Slider 1.0.x versions.

---

## Updating

DevArt Slider uses the standard Joomla update system.

Before updating a production website:

- Create a complete backup
- Test the update on a staging environment
- Verify the component administrator
- Verify module output
- Verify all content sources used by the website
- Clear frontend and CDN caches when necessary

Version 1.0.8 is a safe update from previous 1.0.x releases and does not introduce database schema changes.

---

## Version 1.0.8 Highlights

DevArt Slider 1.0.8 introduces a major improvement to Joomla Article selection.

Highlights include:

- New Joomla-style modal article selector
- Multi-article selection
- Multi-page persistent selection
- Fast article search
- Previous and next page navigation
- Selected article ordering
- Add Selected and Done workflows
- Removal of full article table preloading
- Bounded two-phase article loading
- Major reduction in administrator memory use
- Resolution of administrator article selector timeouts
- Correct Joomla MVC state initialization
- Compatibility with existing slider configurations
- Validation on a Joomla installation containing more than 220,000 Articles

---

## Large-Site Validation

DevArt Slider 1.0.8 was tested using a Joomla installation with more than **220,000 native Joomla Articles**.

The following operations were verified:

- Opening a new slider
- Editing an existing slider
- Opening the Selected Articles modal
- Loading the latest article page
- Searching by article title
- Searching by article ID
- Changing page size
- Navigating through article pages
- Selecting articles from multiple pages
- Adding selected articles while continuing to browse
- Completing selection with Done
- Removing selected articles
- Reordering selected articles
- Saving and reopening the slider
- Preserving article IDs and ordering
- Rendering the resulting slider on the frontend

The selector remained fast without increasing PHP memory or execution time limits.

---

## Important Performance Principle

DevArt Slider never attempts to make a large website usable by simply increasing PHP limits.

Instead, the extension uses bounded application architecture:

- Query only the records currently required
- Never preload complete content tables
- Apply hard result limits
- Use server-side pagination
- Resolve only stored selected IDs
- Reuse cached frontend output
- Avoid unnecessary administrator work
- Keep frontend and administrator responsibilities separated

This approach makes performance predictable and allows the extension to scale with the website’s content volume.

---

## Compatibility

DevArt Slider is designed for:

- Joomla 6.x
- PHP 8.3+
- Modern MySQL and MariaDB environments
- Joomla Atum administrator template
- Responsive frontend templates
- Cloudflare
- Reverse proxies
- CDN environments
- Small business websites
- Municipal and organizational websites
- Editorial websites
- Magazine portals
- Large news websites
- High-traffic Joomla installations

---

## Support and Documentation

Project repository:

https://github.com/devartgr/joomla-devart-slider

Website:

https://devart.gr

Before reporting an issue, include:

- Joomla version
- PHP version
- Database type and version
- DevArt Slider version
- Slider source type
- Slider template
- Relevant error message
- Steps required to reproduce the issue

Do not include passwords, private keys, access tokens, or other sensitive information.

---

## License

DevArt Slider is released under the GNU General Public License version 3 or later.

See the included license file for complete licensing information.

---

## Author

**Stathopoulos Kostas — DevArt**

Website: https://devart.gr
