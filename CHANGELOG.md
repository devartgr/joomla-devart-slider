# Changelog

## 2.0.2 - 2026-10-31

Cache resilience, Events source reliability, multi-card image polish, and Sources companion **1.0.1**. Requires Joomla 6.0+ and PHP 8.3.0+. No database schema changes. Bundled `pkg_devartsources` upgrades to **1.0.1** when missing or older (never downgrades).

- Fix: remove thumb encode `.lock` after flock; Clear image cache + retention GC also delete `.lock`/`.tmp` orphans.
- Fix: after Clear image cache, multi-card sliders encode **primary** thumbs first (budget 8) instead of burning the request budget on srcset sizes of the first card (other cards no longer fall back to the original image).
- Fix: multi-card refresh — eager + high fetchpriority + sync decode for all above-the-fold cards; paint SSR immediately; upgrade infinite clones only after those images are ready (no track hide, no 2nd/3rd-card flash).
- Perf: `PluginSourceAdapter` uses `SliderCache::remember()` (stale-while-revalidate + single-flight), matching Custom Lists.
- Fix: Video Sources random uses bounded pool + shuffle (no SQL `RAND()`); pin refreshed Sources companion.
- Fix: Events `publish_down` parity with Events 1.1.4 Visibility (Slider warm cache + Sources Events provider; Widgets warm cache aligned).
- Fix: Events source empty FE — Sources `EventsQuery` calls `applyOrderJoin()` (Events `orderSql` stub alone caused `Unknown column edo.sort_start` / `query_failed`); fail-closed when event category mode is selected with an empty list.
- Fix: pin Sources companion **1.0.1** so Slider install upgrades Sites that already have Sources `1.0.0` (same-version companion previously skipped the Events query fix).
- Fix: `SliderCache::remember()` keeps serving stale slides when SWR revalidation throws (temporary DB/provider failure); cold miss still fails closed.
- Fix: `fillSingleFlight()` sets `servedFromCache` when returning a disk payload filled by another request (so warm visibility checks still run).
- Perf: request-memoize `getTableColumns` in `CachedItemVisibility`; sort access levels in Custom List cache keys (parity with plugin adapter).
- Docs: System Page Cache caveat + thumb retention GC / Scheduled Task hint in `docs/cloudflare-caching.md`.
- Test: SWR stale-on-revalidate-failure, cold-miss exception, fillSingleFlight `servedFromCache` disk hit.

## 2.0.1 - 2026-10-27

M7 plugin-only cut for shared sources. Removes in-product Articles/Business/Events/Video legacy fetch paths, shadow compare, and the Options `source_engine` / `shadow_compare_percent` fields. Installer forces `source_engine=plugin`. Shared sources fail closed (empty) when Sources is unavailable. Host-local `custom` / `custom_slides` stay in-product. No official update-server downgrade — keep **2.0.0** ZIP on GitHub for manual rollback only.

- Fix: clearing Exclude categories / tags / category multi-selects persists as empty (fancy-select omitted POST no longer restores previous settings).

## 2.0.0 - 2026-10-01

Public jump from **1.1.8** (no public 1.2.0). Soft cutover: Options default `source_engine=plugin` with legacy/shadow retained and auto-fallback. Build embeds pinned `pkg_devartsources` 1.0.0 (`companions/`); installer installs/upgrades Sources when missing/older (never downgrades). Host-local `custom` / `custom_slides` stay on legacy.

- Fix: touch actively served thumbs (daily) so 30-day retention GC does not delete hot files.
- Test: Node JS smoke for site-core init ordering (default + showcase); wired into `validate.php`.
- Perf: stale-while-revalidate for slide cache (`remember()` refreshes under lock; `get()` serves fresh+stale until hard grace).
- Refactor: SLD-R9 — admin `SourceNormalizer::hydrateFormItem` delegates to site `SourceConfigNormalizer`; `CANONICAL_TYPES` aliases `SourceFactory`.
- Fix: SliderSettingsNormalizer dedupes positive IDs in selection lists.
- Perf: multi-card templates emit template-aware `sizes` for srcset (desktop card count → vw); Cloudflare docs add purge/invalidation notes.
- UI: remove drop shadow from slider arrow buttons across templates.
- Feature: Settings → Show pause/play button (`autoplay_pause_button`, default on) for the N7 WCAG autoplay toggle.
- Fix: Custom Lists resolve grouped items via `SourceEngine` (honours Options `source_engine` plugin/shadow with per-group legacy fallback).
- Fix: `validate.php` fails if `Version.php` or `joomla.asset.json` are missing (SLD-R6 hardening).
- Fix: article hot-cache visibility requires published `com_content` category (INNER JOIN + access/language).
- Fix: Events fallback fail-closed when selected categories cannot be applied; bound fallback rows to 500; apply featured in fallback.
- Fix: Custom Lists skip redundant visibility on cold fetch; keep filter on warm cache.
- Fix: incomplete thumb budget sets soft slide-cache TTL (45s); skip caching empty plugin payloads; preserve PNG/WebP/GIF alpha in thumbs.
- Feature: Content → Category uppercase toggle (`category_uppercase`, default on) via CSS `--devart-slider-category-transform` for article/business/events/video kickers.
- Fix: Devin P1 SLD-R2/R3/R4/R5 — wire `date_type` in form/KEYS; Business category filter via EXISTS; shadow parity identity-only; Events helpers via `::class`.
- Fix: site-core `initRoot` marks ready only after a template handler exists (deferred template scripts can boot after core).
- Fix: block protocol-relative URLs in `safeUrl()` (`//…`); avoid double-escaping pre-sanitized srcset.
- P4: Admin marker-gated GC deletes expired `slider-*.cache` older than `cache_minutes * 2` (batched).
- P8: Split frontend JS into `site-core.js` + per-template modules loaded by `loadAssets($template)`; add `sql/updates/mysql` schema path; CachedItemVisibility logs when an integration table is missing.
- P5: PHPUnit coverage for SliderCache (key/TTL/atomic), CachedItemVisibility fail-closed paths, import→normalizer regression; `scripts/validate.php` runs PHPUnit before build.
- P2: Slide `<img>` tags emit `width`/`height`, `fetchpriority`/`decoding`, and `srcset`/`sizes` when cached thumbs are available.
- P3: Thumbnails prefer WebP (GD `imagewebp`, quality 80) with JPEG fallback; Cloudflare Edge TTL docs for thumbs and FPC caveats.
- P1: Cap `custom_slides` (100) and ID lists at 200 in SliderSettingsNormalizer; runtime SourceConfigNormalizer mirrors caps.
- P6: Per-slide try/catch + SafeLog so one bad slide cannot blank the whole slider.
- M6: Slider host adapter for `pkg_devartsources` (`legacy` / `shadow` / `plugin`); maps Articles, Video, Business, Events to `SliderSlide`.
- N4: `scripts/validate.php` asserts `Version::VERSION` and `joomla.asset.json` match package version.
- N6: Site i18n for empty slides + default read more (en-GB/el-GR); slideshow pause/play a11y strings.
- N7: Autoplay pause control + IntersectionObserver gate across slider inits (WCAG 2.2.2).
- N8: `mod_devartslider` migrated to AbstractModuleDispatcher + services/provider.php.
- N9: PHPUnit unit suite (Normalizer, CacheTtl, safeUrl/safeMediaUrl).
- N3: ImageResolver caps new thumbnail encodes to 3 per request.
- N5: VideoSource memos `getTableList` / `getTableColumns` per request lifetime.
- Fix: `image_fallback` when file missing; strip `#joomlaImage://`; Events/Business prefer logo when image empty.
- N2: CachedItemVisibility re-checks Business/Events/Video on cache hit.
- N1: Import/save share template/theme allowlists and language length cap via SliderSettingsNormalizer.
- Widgets Data catch-up: Events `events_time_filter=featured`; dedicated `video_featured`.
- Shadow soak: PluginSourceAdapter Sources-contract filters; legacy route_query + ItemRouteHydrator; shadow sample % default 10.
- AS/AR/AQ/AP: normalizer shared paths, Custom list batch resolve, SafeLog, CacheTtl, Media ACL, atomic thumbs.

## 1.0.9 — 2026-08-03

Fixed administrator New/Edit Slider failures on sites without optional DevArt integrations installed.

- Replaced unguarded Business, Events and Video category `sql` form fields with guarded `IntegrationCategory` fields
- Optional integrations are detected by both component availability and category table existence before any query runs
- Unavailable integrations no longer break the Slider form; source types are hidden unless already saved on the slider
- No database schema changes
- Article modal architecture, selected_articles storage and frontend source queries remain unchanged

## 1.0.8 — 2026-08-03

Fixed administrator memory exhaustion on large Joomla sites by replacing the unbounded `selected_articles` SQL field with a bounded Joomla-style multi-article modal selector. Existing `selected_articles` integer array storage remains unchanged.

Performance hardening for the Select Articles modal on sites with 220,000+ articles:

- ID-first two-phase SQL (bounded ID query, then detail fetch for page IDs only)
- Approximate previous/next pagination with no `COUNT(*)`
- Deterministic modal state (`a.id DESC`, fresh-session reset, no stale ordering)
- Lightweight modal filters only (search, published/state, limit)
- Category and language modal filters deferred to a future bounded-filter milestone
- Skip thumbnail cache cleanup on modal requests

## 1.0.7 — 2026-07-07

Repository bootstrap milestone. Real extension sources imported into the DevArt Repository Template v1.0.0 workflow. Package inventory normalized to `com_devartslider` and `mod_devartslider`. PHP minimum raised to 8.3.0 across manifests and installer scripts.

Detailed product change notes for version 1.0.7 were not documented in the repository source at bootstrap time.

## 1.1.8 and earlier production notes

See package `changelog.xml` / prior GitHub releases for 1.1.x production entries.
