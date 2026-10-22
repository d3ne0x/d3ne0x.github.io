# XELO Labs website design system

The shared stylesheet is `/assets/css/xelo.css`. Edit this file to change global colours, spacing, typography, cards, buttons, navigation, footers or responsive behavior.

## Page structure

Every product page uses: skip link, site header with XELO LABS mark, main content, product hero, feature grid, release/download status, product About, support link, and site footer.

For a new tool:
1. Create `/<product-slug>/index.html`, copying `packet-monitor/index.html`.
2. Update page title, description, hero, feature names, requirements, download availability and product-specific About.
3. Add a new card inside the homepage Applications catalogue.
4. Keep `<link rel="stylesheet" href="/assets/css/xelo.css">` and shared navigation/footer markup in sync.
5. Link downloads only to public, verified release assets; never link public visitors to private repositories.

## Brand tokens

Navy `#092f44`; teal `#008b91`; deep teal `#006f78`; ink `#10384b`; muted `#53717e`; paper `#f7faf9`; border `#dce8e9`; card radius `16px`. These are defined as CSS custom properties in `:root`.

## Reusable CSS components

`.container`, `.site-header`, `.header-inner`, `.site-logo`, `.logo-mark`, `.nav`, `.hero`, `.product-hero`, `.eyebrow`, `.lead`, `.section`, `.grid`, `.card`, `.meta`, `.button`, `.button.secondary`, `.button-row`, `.info-panel`, `.product-content`, `.site-footer`, `.footer-inner`, `.skip-link`.

Keep contrast, text alternatives, keyboard focus indication and mobile layout intact. The brand X is a typographic placeholder, not the previously approved PNG artwork.

## Site platform

Static GitHub Pages, no external dependencies. The current pages share CSS and conventions, but header/footer HTML is duplicated because there is no template engine. When the catalogue grows, consider a static-site generator (e.g. Jekyll) for shared partials.
