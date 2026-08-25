# Lavaserv visual system

This document records the shipped multi-route marketing surface in `src/pages/`, the shared layout in `src/layouts/BaseLayout.astro`, the shared components in `src/components/`, and `src/styles/global.css`.

## Direction

The visual world is formal local technical service: confident, direct and highly legible. The system uses the old site's blue palette as a continuity anchor, with a restrained version-five home page built around coverage blocks, large practical copy, real route navigation and a clear WhatsApp path.

## Palette

- Deep service blue: `#044cab` — header CTA, technical panel, process section, primary text accents.
- Electric blue: `#0093ed` — emphasis, service strip, secondary action surfaces.
- Cool paper: `#f6f8f5` — main page background.
- Ink: `#142132` — display text.
- Muted slate: `#5d6b78` — supporting copy.
- White: `#ffffff` — contrast surfaces and CTA text.

## Typography

Barlow Condensed is self-hosted through the project for strong, practical headlines; Manrope is self-hosted for supporting copy. Headlines are large, tight, and sentence-led; supporting copy stays short and readable.

## Components

- Header: real circular Lavaserv seal plus a compact wordmark, route navigation, active-state treatment, and one persistent booking CTA. The same seal is reused in the footer and as the browser icon.
- Home: a formal coverage-led hero with embedded technician photography, WhatsApp/phone actions, direct fault shortcuts, services, process, coverage, FAQ, and final CTA.
- Routes: `/servicios/`, `/servicios/lavadoras/`, `/nosotros/`, and `/contacto/` each carry a distinct visitor question without breaking the visual system. Service, washer, and about routes use an appropriately placed supporting photograph, not a generic gallery.
- Photography: local JPG sources live in `src/assets/images/`, reduced before use and emitted by Astro as responsive AVIF/WebP variants. The about route makes the home-visit moment visible; the services route uses a dishwasher diagnosis only as contextual support for its final consultation CTA.
- Contact: a zero-backend qualifier form creates a prefilled WhatsApp message for the chosen appliance, commune, and symptom.
- WhatsApp: a floating direct-contact button remains prominent at every size and becomes a larger compact bubble on mobile.
- Icons: one authored stroke-icon system keeps contact and directional affordances consistent.

## Interaction and accessibility

All lead links use real WhatsApp or phone URLs and push a `generate_lead` event to `window.dataLayer` when available. Focus rings are visible, the layout responds below 900px and 620px, and reduced motion disables nonessential motion. The diagnostic-fault list has one progressive reveal, while photography stays static and has reserved space to avoid layout shift.
