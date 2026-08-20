# DevArt Slider for Joomla

Professional multi-source slider solution for Joomla 6, designed for news portals, magazines, publishers, municipalities, organizations, business websites, agencies, and high-traffic production environments.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.3%2B-green)
![Release](https://img.shields.io/badge/Version-1.1.4-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Slider is a modern Joomla 6 slider component and module built for creating responsive, professional content sliders from multiple Joomla and DevArt content sources.

The extension is designed for production websites where performance, stability, responsive rendering, administrator usability, and safe integration handling are essential.

DevArt Slider supports:

- Joomla Articles
- Manually created Custom Slides
- Reusable **Custom Lists** (mixed sources)
- DevArt Business
- DevArt Events
- DevArt Video

All content sources use a unified rendering architecture.

The extension includes multiple production-ready templates, configurable themes, image processing, frontend caching, responsive controls, Joomla-native Trash for sliders, and a high-performance Joomla-style article/item selector designed to remain usable even on websites containing hundreds of thousands of articles.

Optional DevArt integrations are detected safely. DevArt Slider does not require DevArt Business, DevArt Events, or DevArt Video to be installed.

---

## Version 1.1.4

DevArt Slider **1.1.4** is the current public package on the **1.1.x** line.

It includes the full **1.1.0** feature set plus installer and administrator UX fixes:

- Safe same-line package downgrades (standalone installer — DevArt pattern; PHP/Joomla minimums only)
- Constrained edit-form control widths so Template/Basic dropdowns are usable (builders and editors stay full width)
- No database schema changes from 1.1.0

### Version 1.1.0 Highlights

- **Custom Lists** — reusable mixed-source lists with administrator submenu and frontend resolution
- **Widgets Data parity** — unified source types, Categories vs Specific items, shared item picker; Articles advanced filters (tags, author, date, ordering)
- **Sliders Trash** — Joomla-native trash (`published = -2`), Published / Unpublished / Trashed filters; permanent delete only from Trash
- **Security & hardening** — non-webroot query cache, media upload validation, ACL tightening, bounded random ordering, thumbnail resource caps
- **Languages** — el-GR, fr-FR, de-DE, es-ES, it-IT, pt-PT (administrator, site module, package)
- **14 templates** — frontend QA closed with overlay, transition, and theme polish
- **Admin UX** — Content Simple/Advanced, DevArt tabs/submenu polish, Access & Language on Basic, cleaner Sliders list
- Inline **Custom Slides** preserved as a first-class source alongside Custom Lists
- Package-only Joomla update channel (`pkg_devartslider`)
- Joomla **6.0+** / PHP **8.3.0+** only

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

The article selector has been successfully tested on a production-scale Joomla environment containing more than **220,000 native Joomla Articles**.

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

Joomla native updates target the **package only** (`pkg_devartslider`).

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
- Include/exclude tags, author, and date filters (Categories mode)
- Configurable ordering (including bounded random — no SQL `ORDER BY RAND()`)
- Article limits
- Article skip values

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
- Preservation of existing article IDs and ordering

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

Inline Custom Slides remain a first-class source and are not replaced by Custom Lists.

### Custom Lists

Create reusable mixed-source lists that can combine:

- Joomla Articles
- DevArt Business
- DevArt Events
- DevArt Video
- Custom list items

Custom Lists are managed from the administrator submenu and selected as a slider source (`source_type=custom`). Existing inline Custom Slides configurations remain fully supported.

### DevArt Business

Create sliders from DevArt Business listings with:

- All Categories or Selected Categories
- Specific items selection
- Child category inclusion
- Featured business handling
- Configurable ordering
- Existing slider image and cache pipeline

DevArt Business integration is optional.

The source becomes available only when:

1. The DevArt Business component is enabled.
2. The required DevArt Business category table exists.

When the integration is unavailable, DevArt Slider does not execute category queries against the missing table.

### DevArt Events

Create sliders from DevArt Events with:

- Today
- Upcoming
- Past
- All Events
- Category filtering
- Specific items selection
- Child category inclusion
- Featured event handling
- Event occurrence-aware ordering

Event selection uses the actual DevArt Events date information instead of Joomla article publishing dates.

DevArt Events integration is optional.

The source becomes available only when:

1. The DevArt Events component is enabled.
2. The required DevArt Events category table exists.

### DevArt Video

Create sliders from DevArt Video with:

- All Categories or Selected Categories
- Specific items selection
- Child category inclusion
- Featured video handling
- Newest or Oldest ordering
- Existing slider image, rendering, and cache pipeline

DevArt Video integration is optional.

The source becomes available only when:

1. The DevArt Video component is enabled.
2. The required DevArt Video category table exists.

---

## Optional Integration Safety

DevArt Business, DevArt Events, and DevArt Video are optional integrations.

DevArt Slider does not assume that every DevArt extension is installed on every website.

Before loading categories from an optional integration, the administrator interface verifies:

- That the corresponding Joomla component is enabled
- That the required database table exists

Both conditions must be satisfied before a category query is executed.

When an integration is unavailable:

- No query is executed against its database table
- No missing-table SQL error is generated
- The unavailable source is hidden from new slider configurations
- Existing saved source values remain visible when necessary
- The Slider New/Edit interface continues to load normally
- Joomla Articles, Custom Slides, and Custom Lists remain fully available

This allows DevArt Slider to operate safely on websites using any combination of DevArt extensions.

---

## Slider Templates

DevArt Slider includes **14** responsive, production-ready templates for different website styles and content types.

Available designs include editorial, magazine, news, card, preview, overlay, hero, sidebar, accordion, tiles, and split-content layouts.

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
- Thumbnail resource caps (skip unsafe oversized decode)
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
- Responsive slider presentation
- Integration with DevArt Video content sources

---

## Frontend Performance

DevArt Slider uses a cache-first frontend architecture intended for production and high-traffic websites.

Performance characteristics include:

- Access-aware component query cache (Joomla cache storage, not webroot)
- Versioned JSON cache payloads with purge on save/publish/duplicate/import/delete
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
- Module HTML cache disabled so visibility stays access/language-aware

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
- Guarded optional integration category queries
- No queries against unavailable optional component tables
- Constrained edit-form control widths for usable selects and inputs

These safeguards prevent the memory exhaustion, timeouts, and SQL errors commonly caused by loading large content collections or unavailable integration data during administrator form rendering.

---

## Caching

DevArt Slider includes configurable frontend caching to reduce repeated database and rendering work.

Cache features include:

- Component query cache stored in Joomla cache (non-webroot)
- Configurable cache lifetime
- Cache separation by slider configuration and access/language context
- Automatic purge on slider save, publish, duplicate, import, and delete
- Administrator cache clearing
- Safe handling of empty source results
- Cached thumbnail management under media
- Compatibility with reverse proxies
- Compatibility with CDN environments

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
- Joomla Web Asset Manager (`joomla.asset.json`)
- Joomla Form API
- Joomla ACL
- Joomla database APIs
- Joomla administrator layouts
- JoomlaDialog modal integration
- CSRF protection
- Proper input filtering
- Escaped output

No Joomla 3/4/5 compatibility layer is included.

---

## Security

Security measures include:

- Joomla ACL enforcement (`core.edit.state`, create/edit for duplicate/import)
- CSRF protection for administrator actions
- Input filtering and normalization
- Integer normalization for selected IDs
- Joomla database query APIs
- Parameterized or safely constructed queries
- Output escaping
- Same-origin modal communication checks
- Controlled administrator-only article selection
- Hardened media uploads (MIME/content checks, size limits, images-root confinement)
- Non-webroot query cache with versioned JSON payloads
- Bounded random ordering (no SQL `ORDER BY RAND()`)
- Atomic duplicate/import (database transactions)
- Availability checks before optional integration queries
- Safe package installation and update handling

---

## Permissions

DevArt Slider integrates with Joomla ACL.

Administrators can configure permissions for actions such as:

- Accessing the component
- Creating sliders
- Editing sliders
- Changing slider state (including Trash / Publish restore)
- Deleting sliders (permanent delete from Trash)
- Managing component options

Permission behavior follows Joomla user groups and Joomla ACL conventions.

---

## Import and Export

Slider configurations can be exported for backup or transfer purposes.

Duplicate and import use database transactions and require appropriate ACL (`core.create` and `core.edit`).

Existing Selected Articles data remains compatible with the high-performance modal selector because the stored format is unchanged.

Selected article IDs continue to be stored as an ordered integer list within the slider configuration.

---

## Requirements

- Joomla 6.x (minimum **6.0.0**)
- PHP **8.3.0** or newer
- MySQL or MariaDB supported by Joomla 6
- PHP image processing support according to the Joomla server configuration
- A modern browser for administrator and frontend interfaces

Optional integrations require the corresponding DevArt extension:

- DevArt Business
- DevArt Events
- DevArt Video

The optional integrations are not required for Joomla Articles, Custom Slides, or Custom Lists that only use available sources.

---

## Installation

1. Download the latest package:

   `pkg_devartslider_v1.1.4.zip`

2. Open the Joomla administrator.

3. Go to:

   `System → Install → Extensions`

4. Upload and install the package.

5. Open:

   `Components → DevArt Slider`

6. Create or edit a slider.

7. Publish a DevArt Slider module and select the required slider.

The package supports installation and updates through the standard Joomla Extensions installer.

---

## Updating

DevArt Slider uses the standard Joomla update system (package update server).

Before updating a production website:

- Create a complete backup
- Test the update on a staging environment
- Verify the component administrator
- Verify New/Edit Slider
- Verify module output
- Verify all content sources used by the website
- Clear frontend and CDN caches when necessary

Version **1.1.4** is a safe update from previous DevArt Slider **1.0.x** and **1.1.x** releases.

Typical update characteristics:

- No database schema migration required from recent 1.0.x / 1.1.x (Custom Lists tables are additive)
- Existing slider identifiers and Selected Articles ordering remain compatible
- Inline Custom Slides remain supported
- Packages from **1.1.4** onward allow safe same-line downgrades between themselves

Historical ZIPs that still use the old `InstallerScript` sequence check cannot install over a newer version.

---

## Version History Highlights

### 1.1.4

- Safe same-line package downgrades (standalone installer)
- Constrained administrator edit-form control widths

### 1.1.0

- Custom Lists and Widgets Data parity
- Sliders Trash and list UX
- Security / cache / media / ACL hardening
- Multi-language packs
- Full template QA and admin polish
- Package-only update channel

### 1.0.9

- Safe optional integration detection for Business / Events / Video
- Guarded category loading when optional components are missing

### 1.0.8

- High-performance Joomla-style modal article selector
- Bounded two-phase loading for very large article databases

---

## Large-Site Validation

The high-performance article selector was tested using a Joomla installation with more than **220,000 native Joomla Articles**.

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
- Apply controlled result limits
- Use server-side pagination
- Resolve only stored selected IDs
- Reuse cached frontend output
- Avoid unnecessary administrator work
- Keep frontend and administrator responsibilities separated
- Avoid optional integration queries when dependencies are unavailable

This approach makes performance predictable and allows the extension to scale with the website’s content volume.

---

## Compatibility

DevArt Slider is designed for:

- Joomla 6.x
- PHP 8.3+
- Modern MySQL environments
- Modern MariaDB environments
- Joomla Atum administrator template
- Responsive frontend templates
- Cloudflare
- Reverse proxies
- CDN environments
- Small business websites
- Municipal websites
- Organizational websites
- Editorial websites
- Magazine portals
- Large news websites
- High-traffic Joomla installations

---

## Download

Latest release:

`pkg_devartslider_v1.1.4.zip`

GitHub releases:

https://github.com/devartgr/joomla-devart-slider/releases

Direct download:

https://github.com/devartgr/joomla-devart-slider/releases/download/v1.1.4/pkg_devartslider_v1.1.4.zip

SHA-256:

`a4a2b44f7c15cccb34f5867dc147e3342c8bf2283f4d30a3bc32b73cd7c93405`

Update metadata:

https://raw.githubusercontent.com/devartgr/joomla-devart-slider/main/update.xml

Changelog:

https://raw.githubusercontent.com/devartgr/joomla-devart-slider/main/changelog.xml

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

**Kostas Stathopoulos — DevArt**

Website: https://devart.gr
