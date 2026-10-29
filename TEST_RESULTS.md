# Verification record

Date: 29 October 2026. Engine: Playwright Chromium, isolated temporary browser context. Website served locally over HTTP; a direct file launch was also checked.

Result: **23 checks passed**, zero browser JavaScript errors, zero failed HTTP responses.

- PASS: Six local car photographs, hero and two location photos decode
- PASS: Body filters: Sedan 1, SUV 3, Hatchback 2; reset 6
- PASS: Ascending and descending price sorting, including combined filter
- PASS: Quick search rejects zero-day and 366-day rentals; accepts valid dates
- PASS: Booking opens selected photo and inherits quick-search dates
- PASS: Required fields, invalid email and invalid phone block advancement
- PASS: Daily, weekly and monthly pricing update with unchanged discount rules
- PASS: Past pickup and reversed dates block reservation
- PASS: Demo card step, back navigation and required consent
- PASS: Reservation creates reference and local record
- PASS: Collection, designated return, employee inspection and damage bill
- PASS: Final simulated credit-card payment completes journey and persists after reload
- PASS: No-damage and major-damage inspections with final payments
- PASS: Keyboard dialog focus trap and Escape
- PASS: Responsive width 1440px
- PASS: Responsive width 1024px
- PASS: Responsive width 820px
- PASS: Responsive width 768px
- PASS: Responsive width 390px
- PASS: Responsive width 320px
- PASS: Desktop, tablet and mobile: no page overflow, every image loads, usable navigation
- PASS: No browser JavaScript errors or HTTP failures
- PASS: Direct file:// launch renders all local images and fleet

## Evidence
Fresh PNG captures in `screenshots/` cover homepage, all six fleet cards, reservation form, demo card selection, confirmation, inspection, final bill, locations, mobile booking and tablet. Screenshots use synthetic customer details.

## Limits
The public GitHub Pages deployment was subsequently tested on 29 October 2026; see LIVE_VERIFICATION.md for the separate live results. Real mobile hardware, Firefox, Safari, real inventory, real payments, staff authentication and server persistence were not tested or claimed. CSS viewport emulation covered widths 320, 390, 768, 820, 1024 and 1440 pixels. Test reservations were confined to an isolated browser context and did not change the user’s browser bookings.

## Change preservation
The original six car rates, category values, weekly/monthly discounts, tax calculation, storage key and business-state transitions remain unchanged. JavaScript edits replace asset references, improve image metadata and add access to the existing booking manager from the mobile menu. The original invalid phone-field regular expression was corrected in HTML.

Source comparison against the archived original also confirmed that 22 utility, reservation, storage and rental-flow functions are byte-for-byte unchanged. No student ID was found in the website HTML, CSS, JavaScript, Markdown or JSON files.
