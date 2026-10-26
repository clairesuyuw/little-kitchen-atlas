# Little Kitchen Atlas

An Asian recipe atlas built with **pure HTML5 and CSS3**, with no JavaScript, frameworks, build tools, or runtime data fetching.

Live website: https://pixel-kitchen-atlas.suyuw.chatgpt.site/

## Experience
Choose a country, view the local-language dish name and English translation, and flip its illustrated card for ingredients and steps.

## Files
- `index.html`: semantic layout, inline SVG country links, eight complete recipes, native checkbox controls, and help dialog.
- `style.css`: documented layout sections, Lora headings, DM Sans supporting text, responsive rules, map highlights, and CSS-only interaction states.
- `assets/food-*.svg`: original smooth vector food illustrations.

## Run
Open `index.html` directly, or use VS Code Live Server. No script or JSON fetch is required. Google Fonts requires internet; browser fonts are used when offline. Asian characters may use system fallback fonts.

## How CSS-only interaction works
- Country and journal links target recipe sections using URL fragments and `:target`.
- `:has()` hides the atlas when a recipe is selected and links related map highlights.
- Each recipe uses one native checkbox; clicking its image label or the label below toggles a CSS 3D flip. Keyboard users Tab to the checkbox and press Space.
- The help link targets a nonmodal dialog overlay. Its close link returns to the atlas.
- Browser Back/Forward works with fragment navigation. Checkbox states remain until toggled or reset by the browser.

## Accessibility and behavior limits
Current browsers supporting `:has()` are required. Without JavaScript, the help panel has no scripted focus trap or Escape-to-close behavior, and navigation does not programmatically move keyboard focus. These limitations are documented rather than emulated with hidden scripts. Main map navigation and card flipping are implemented entirely in HTML/CSS. The previous automatic flip reset on country changes is replaced by native checkbox state persistence.

## Credits
Map outlines: Natural Earth via https://github.com/datasets/geo-countries. Simplified culinary overview, not a boundary reference. Food illustrations are original SVG drawings; recipes are simplified home-kitchen versions. AI assisted the implementation through iterative prompts and revisions.
