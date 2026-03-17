# The Colville — Kitchen & Bar | Demo Site

A single-file demo restaurant website with a built-in instant promo distribution tool.

## How it works

Open `index.html` in any modern browser. No server required.

### The Promo Tool

1. Click the **PROMO TOOL** tab on the right edge (or wait — it auto-opens after 1.5s)
2. Fill in the form: title, description, price, dates, CTA
3. Choose a **tone of voice** from the four options
4. Hit **PUBLISH PROMO** and watch the site update in real time:
   - The scrolling ticker updates
   - An announcement bar slides in below the nav
   - A new event card appears in the What's On section
   - The panel shows generated social/email copy ready to copy

### Tone Templates

Four tone variants generate platform-specific copy for Instagram, Facebook, and Email:

| Tone | Style |
|------|-------|
| Refined & Elegant | Formal, understated, luxury hospitality voice |
| Warm & Inviting | Friendly, welcoming, personal |
| Bold & Playful | Punchy, energetic, emoji-forward |
| Casual & Friendly | Relaxed, approachable, conversational |

Templates use simple string interpolation — `{title}`, `{description}`, `{price}`, `{dates}`, `{cta}` are replaced from the form fields.

## Adding a real AI API later

To replace the templates with AI-generated copy:

1. Add an API key input or environment config
2. Replace the `generateCopy()` function to call your API (e.g. Claude, GPT)
3. Send the promo data + selected tone as a prompt
4. Display the API response in the existing output UI

The output UI (tabs, copy buttons, character counts) stays the same — only the copy generation source changes.

## Customisation

- **Colours:** Edit the CSS custom properties in `:root` at the top of the `<style>` block
- **Fonts:** Swap the Google Fonts `<link>` and update `--font-display` / `--font-body`
- **Images:** Replace the Unsplash URLs with your own photography
- **Restaurant details:** Update the footer address, hours, and content throughout
- **Tone templates:** Edit the `toneTemplates` object in the `<script>` block

## Tech

- Zero dependencies — vanilla HTML, CSS, JS
- Google Fonts (Cormorant Garamond + Outfit)
- Unsplash images via CDN
- No build step, no framework, no server
