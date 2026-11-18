WATTALYZE — INTERFACE REVISION

RUN
Extract the ZIP. Keep index.html, account.html, style.css and app.js together. Open index.html, or open the folder in VS Code and use Microsoft Live Preview. For GitHub Pages, replace all four files in the publishing folder and commit. A hard refresh may be needed after deployment. No npm or build step.

CHANGES
- Removed main hero heading and introduction.
- Added smaller, lighter tagline immediately next to the logo.
- Renamed section 1 to Household information / Thông tin hộ gia đình.
- Removed the example introduction and dormitory paragraph from section 1.
- Removed the water-heating selector and its hidden gating of calculations. Optional electric water heater is now an ordinary appliance, default quantity zero in all presets.
- Removed requested instruction sentences and Source/Brand-model columns. Removed source completeness statistics.
- Renamed AC family and everyday family profiles in Vietnamese.
- Translated kWh/year and kWh/cycle throughout Vietnamese labels, selectors, and explanations.
- Added concise section 4 bullet instructions.
- Removed replacement-specification introduction.
- Renamed Action preference to Recommendation priority / Ưu tiên khuyến nghị; expandable explanation included.

PRESERVED
Language and theme switches, linked account page, browser-local history, action plans, export/deletion, three editable presets, variable recommendations, tariffs/VAT, real-bill comparison and calculation explanations.

MODEL NOTES
Appliance defaults and replacement specifications are editable examples. Presets are not measured households. Basic assumptions remain in About and calculation explanations.
Power calculation: quantity × average electrical watts × hours/day × days / 1000.
Annual-label calculation: quantity × kWh/year × days / 365.
Cycle calculation: quantity × kWh/cycle × cycles/week × days / 7.
No appliance age/brand multiplier. Refrigerator watts must represent whole-day average if power mode is used.
Bill is not used to force appliance estimates to match. Monetary scenarios use billed kWh if entered, otherwise modeled consumption. Other loads and fixed charges are held unchanged. Recommendations are independent and their savings must not be added.

BILLING
Preserved published defaults effective 2026-11-01: block widths 100,100,200,300,remainder; rates 1901,2289,2894,3456,3844 VND/kWh before VAT; VAT default 8%, editable. Sources are linked in About. No automatic tariff updates. Monthly household thresholds are not rescaled by billing days. Special periods, allocations and price transitions need separate checking. Custom dormitory rate is illustrative, not verified. If a flat rate includes VAT, use VAT=0. Other fixed charge is a final amount, not taxed again.

ACCOUNT
No online authentication/cloud storage. Data stays in local browser storage; do not enter passwords or sensitive identifiers. Example account records remain labeled separately from saved records. Uses the previous v2 storage keys to preserve same-origin history; old source/model metadata is ignored on load. Moving origins (file to localhost or GitHub) does not transfer browser storage.

TESTS
Automated Chromium tested three presets, independent optional water-heater calculation, removed controls, Vietnamese unit translation, theme, history/actions, loading saved inputs, and 390px layout. Ten numerical checks passed; no page errors in tested flows. These tests verify implementation, not real-world energy prediction accuracy.
