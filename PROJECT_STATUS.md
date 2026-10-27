# Project
DevArt Slider — Modern Joomla 6 slider package with support for Joomla Articles, DevArt Video and other content sources.

# Repository Status
**2.0.1** published on GitHub (`v2.0.1`); update channel advertises **2.0.1**. Latest VPS-confirmed baseline remains **2.0.0** until VPS QA for 2.0.1 is confirmed.

# Current Version
`2.0.1` (GitHub **v2.0.1** published; VPS QA pending for milestone close)

# Package
`pkg_devartslider`

# Extension Inventory
- `com_devartslider`
- `mod_devartslider`

# Verified Package (latest VPS OK)
`builds/pkg_devartslider_v2.0.0-rc_879c2fd0.zip`  
(also `builds/pkg_devartslider_v2.0.0.zip` / local `releases/pkg_devartslider_v2.0.0.zip`)

# Verified SHA-256 (2.0.0 RC — Sources companion + soft plugin default)
`879c2fd05b1d57a7b04dfd55fc0a83df2e3ce2a8b108d19210445fc274d173d6`

# Verified Creation Date
`2026-10-01`

# Bundled Sources pin
`pkg_devartsources` **1.0.0** — SHA-256 `40ba16f9b975f2f7a192ae10a9e8d66738d6e580c6ecdda0153344c9c0135411`

# Local Release Copy (public production)
`releases/pkg_devartslider_v2.0.1.zip`  
(previous: `releases/pkg_devartslider_v2.0.0.zip` — keep for manual rollback)

# Last Published GitHub Release
`v2.0.1` — public update.xml advertises **2.0.1**.

# Public update.xml (production)
https://raw.githubusercontent.com/devartgr/joomla-devart-slider/main/update.xml  
(advertises `2.0.1`)

# Verification Status
**2.0.0** VPS confirmed (2026-10-01): soft cutover — Options default `source_engine=plugin` (explicit legacy/shadow preserved on upgrade); build embeds pinned Sources; installer installs/upgrades Sources when missing/older (never downgrades). Includes prior soak (SWR, SLD-R9, sizes/CF, UI controls, CustomList SourceEngine, review-close, category uppercase, Devin R2–R5, JS/safeUrl, P/N). Host-local `custom` / `custom_slides` remain legacy. Root `update.xml` advertises **2.0.0**.

Previous production baseline was **1.1.8**.

# Last Completed
Slider **2.0.1** published on GitHub (`v2.0.1`): M7 plugin-only + admin clear multi-select fix. Artifact SHA-256 `31f3c29ccbfd1468fbe0c6948f32a80094c6780ab0e0740e6d4aa2f4fd5775dd`. Local Herd + harness QA green. **VPS QA pending** before closing milestone / marking verified.

# Current Milestone
Awaiting VPS confirmation for **2.0.1**.

# Next candidates
1. VPS install/QA for **2.0.1** → close milestone / update verified package fields.
2. **Events `publish_down` parity (from DevArt Events 1.1.4 audit):**
   `CachedItemVisibility` calls `visibleIntegrationIds(..., false)` for events (skips
   `publish_down`). After Events 1.1.4, `com_devartevents` Visibility uses both
   `publish_up` and `publish_down`. Align Slider events visibility with Events + Sources
   Events provider in one coordinated milestone (also Widgets).
3. Optional standalone Sources public repo/release if operators need it outside host packages
4. Widgets: `image_fallback` field (separate product task if needed)

# M7 policy (shipped in 2.0.1)
- **Goal:** plugin-only runtime for shared sources; delete legacy Article/Business/Events/Video source classes and shadow compare.
- Host-local `custom` / `custom_slides` remain in-product.
- **No official downgrade** via update.xml / Joomla update server.
- **Safety net:** keep `2.0.0` on GitHub Releases for **manual** reinstall only.
- Sources companion continues never-downgrade.

# Update Channel — Pending External Actions
- Public Slider channel is **v2.0.1**.
- Public Widgets channel is **v2.0.0** (same Sources pin).
- Keep **v2.0.0** ZIP on GitHub for manual rollback only (no update-server downgrade).
- Standalone Sources `update.xml` not published (companion-only distribution).

# Widgets Parity Reminder
Slider retains **inline Custom Slides** (`custom_slides`) as a first-class source. Widgets Data parity must not remove or break it. See `docs/roadmap-widgets-data-parity.md` and `docs/source-engine.md`.

# Previous Production Baseline
`1.1.8` — `pkg_devartslider_v1.1.8.zip`  
SHA-256: `9a4bb5d5200f27794aeb97d401a51162d429e666fb8e1479fc20138fc48d3898`

# Superseded artifacts (pre-2.0.0 soak line)
- thumb-js `f9712b1261270d77b5e8a8638f1f19d875421ec43bde0fc4c07551ef87cbfdbb`
- SWR+R9 `9f4e6f36c3d158a66e1394445d5b6684f2e5bad229ee57c01ab3a8dcf36780b0`
- Sizes-CF `3584e96fed5bec9c7b18c66cc532d0b6481c94bc771b4030e76b5807ee242e77`
- UI-ctrl `5aa12c621a6a8fe95678aaac7bd0c4a7a645a4c63116dd66510f874d327d4055`
- CL-engine `50b5e18586d795453e831981244e7bff759d84f346c5afe81c308d8ef12f3676`
- Review-close `fffaff67c727367183c27d47f0f8cb5b09ed4efc856b110701d444190e5be842`
- Catcase `5a141d64d0c7a6ffc94f6ec2bff843e2d0e6c878d735fa3f1525fc6c7b198dd6`
- R2–R5 `56cb1d9ecfe77ff2593d054f77a1fc7a380568f0b3ca591fa810cb855fdbffe0`
- JS+safeUrl `cef04a8ead6da1b358d58517ea1f4fe5635505036637b219570e7c20f3d41aab`
- P4+P8 `47ecae0d535826ea82fe2fa48cf70b8685b390fba03ca6c5b6028e16c1b64782`
- P5 `68a760822e3e37a789240b779909119be3b3f0c27a86dfd5a3fff74cef913a55`
- P2+P3 `f8670854831eaa8744eca445ce96abcb8e657dff6dab97af4cb1405807431b5d`
- P1+P6 `1ad9628a3a47bc8c9b14702ac17d173a3422d18a5700445361b3ef1c82f90511`
- N4–N9 `7e936b51db1c6f4e416ab323b7d7e3c0aed2436ab5eb88e85c51b701c5bfb916`
- N3+N5+fallback `3e79710a6109224f30c252e5b6a7a53ff200c1504e4212e26b6f8cdc4425faea`
- N1+N2 `0aec18ff5b7ec98bfa66b6a0533765aca37e9f84bf2437a704bdde1cca906810`
- Data catch-up `3562ef553fbf15fa53ce97be63e5c51511b6ae42e87f12d404a8ed015295cad3`
- Soak/plugin `cef87a81e7203e1c918d1fe716609fb63f7e495cab675d6f1620627c8035780a`
- AS `f87ff862a2ea68b50e675694ae7983bc93833e656e76be6e5ee9abee78f65b79`
- AR `cc8f54ae0d67546a7aac20b047bf71834ecf4a903790366090a372d95e2ee294`
- AQ `0800a9bcc731c6e4f13ef9534d48d1a003027fa46737827bbb6ede9f483b144a`
- AP `bff6e24273d8310e0b664c876ef7a9dd66c3ede881af045608d0bb2c5e414e88`
- AN `db603ee3fd373f10326bae15d12abb1c4e2be29aec6f2137602184b990027c9b`
- M6 `6f0b99481347536e044a55e905f8b791c71e31c2fb6173d60dbbfb15476f28c6`
