# DevArt Slider for Joomla

Professional multi-source slider solution for Joomla 6, designed for news portals, magazines, publishers, municipalities, organizations, business websites, agencies, and high-traffic production environments.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.3%2B-green)
![Release](https://img.shields.io/badge/Version-1.0.9-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Slider is a modern Joomla 6 slider component and module built for creating responsive, professional content sliders from multiple Joomla and DevArt content sources.

The extension is designed for production websites where performance, stability, responsive rendering, administrator usability, and safe integration handling are essential.

DevArt Slider supports:

- Joomla Articles
- Manually created Custom Slides
- DevArt Business
- DevArt Events
- DevArt Video

All content sources use a unified rendering architecture.

The extension includes multiple production-ready templates, configurable themes, image processing, frontend caching, responsive controls, and a high-performance Joomla-style article selector designed to remain usable even on websites containing hundreds of thousands of articles.

Optional DevArt integrations are detected safely. DevArt Slider does not require DevArt Business, DevArt Events, or DevArt Video to be installed.

---

## Version 1.0.9

DevArt Slider 1.0.9 is a compatibility and stability hotfix for optional DevArt integrations.

The update prevents administrator SQL errors on websites where one or more optional DevArt components are not installed or their required database tables are unavailable.

### Version 1.0.9 Highlights

- Safe optional integration detection
- Guarded DevArt Business category loading
- Guarded DevArt Events category loading
- Guarded DevArt Video category loading
- No queries against missing optional integration tables
- Unavailable optional source types hidden from new configurations
- Existing saved source values preserved when an integration becomes unavailable
- No database schema changes
- No frontend rendering changes
- No changes to the high-performance article selector introduced in version 1.0.8
- Existing sliders and settings remain compatible

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

### DevArt Business

Create sliders from DevArt Business listings with:

- All Categories or Selected Categories
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
- Joomla Articles and Custom Slides remain fully available

This allows DevArt Slider to operate safely on websites using any combination of DevArt extensions.

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
- Responsive slider presentation
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
- Guarded optional integration category queries
- No queries against unavailable optional component tables

These safeguards prevent the memory exhaustion, timeouts, and SQL errors commonly caused by loading large content collections or unavailable integration data during administrator form rendering.

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
- Compatibility with reverse proxies
- Compatibility with CDN environments

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
- SearchTools-compatible administrator interfaces
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
- Protected cache directories
- Safe package installation and update handling
- Availability checks before optional integration queries

---

## Permissions

DevArt Slider integrates with Joomla ACL.

Administrators can configure permissions for actions such as:

- Accessing the component
- Creating sliders
- Editing sliders
- Changing slider state
- Deleting sliders
- Managing component options

Permission behavior follows Joomla user groups and Joomla ACL conventions.

---

## Import and Export

Slider configurations can be exported for backup or transfer purposes.

Existing Selected Articles data remains compatible with the high-performance modal selector because the stored format is unchanged.

Selected article IDs continue to be stored as an ordered integer list within the slider configuration.

---

## Requirements

- Joomla 6.x
- PHP 8.3 or newer
- MySQL or MariaDB supported by Joomla 6
- PHP image processing support according to the Joomla server configuration
- A modern browser for administrator and frontend interfaces

Optional integrations require the corresponding DevArt extension:

- DevArt Business
- DevArt Events
- DevArt Video

The optional integrations are not required for Joomla Articles or Custom Slides.

---

## Installation

1. Download the latest package:

   `pkg_devartslider_v1.0.9.zip`

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

DevArt Slider uses the standard Joomla update system.

Before updating a production website:

- Create a complete backup
- Test the update on a staging environment
- Verify the component administrator
- Verify New/Edit Slider
- Verify module output
- Verify all content sources used by the website
- Clear frontend and CDN caches when necessary

Version 1.0.9 is a safe update from previous DevArt Slider 1.0.x releases.

The update introduces:

- No database schema changes
- No frontend rendering changes
- No Selected Articles storage changes
- No changes to existing slider identifiers
- No changes to saved article ordering

---

## Version 1.0.9 Highlights

DevArt Slider 1.0.9 improves compatibility with websites that do not have every optional DevArt integration installed.

Highlights include:

- Safe DevArt Business availability detection
- Safe DevArt Events availability detection
- Safe DevArt Video availability detection
- Guarded optional integration category selectors
- Component availability checks
- Required database table checks
- Prevention of missing-table SQL errors
- Safe administrator form rendering
- Hidden unavailable source types for new configurations
- Preservation of existing saved unavailable source values
- Full compatibility with Joomla Articles
- Full compatibility with Custom Slides
- No changes to the article selector introduced in version 1.0.8

---

## Version 1.0.8 Highlights

DevArt Slider 1.0.8 introduced a major improvement to Joomla Article selection.

Highlights include:

- Joomla-style modal article selector
- Multi-article selection
- Multi-page persistent selection
- Fast article search
- Article ID search
- Previous and next page navigation
- Selected article ordering
- Add Selected workflow
- Done workflow
- Removal of full article table preloading
- Bounded two-phase article loading
- Major reduction in administrator memory use
- Resolution of administrator article selector timeouts
- Correct Joomla MVC state initialization
- Compatibility with existing slider configurations
- Validation on a Joomla installation containing more than 220,000 Articles

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

`pkg_devartslider_v1.0.9.zip`

GitHub releases:

https://github.com/devartgr/joomla-devart-slider/releases

Direct download:

https://github.com/devartgr/joomla-devart-slider/releases/download/v1.0.9/pkg_devartslider_v1.0.9.zip

SHA-256:

`d4207353cdd59e682e787d8eb5ae436ad96d18400252835ab89150bdcea8f82d`

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
