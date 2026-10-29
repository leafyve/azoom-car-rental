# Live deployment verification

- Result: **PASS**
- Date: 29 October 2026
- Public website: https://leafyve.github.io/azoom-car-rental/
- Public repository: https://github.com/Leafyve/azoom-car-rental
- Tested website commit: `90dfcd37d999f7f5c22e8afc473ce0d0e0739f20`
- Successful Pages run: https://github.com/leafyve/azoom-car-rental/actions/runs/40844312458
- Pages source: `main`, root `/`; HTTPS enforced.

## Public-browser tests

All tests below used the actual public Pages URL in an isolated Playwright Chromium browser context, with synthetic demo details. The homepage returned HTTP 200, and the dark-green computed CSS style was checked. All six car photographs, the hero and both Singapore photographs decoded successfully.

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

Result: **22 checks passed**, zero browser JavaScript errors, zero failed HTTP responses or browser requests.

## Published-file audit

The homepage HTML, stylesheet, JavaScript, credits page, ten WebP files and two font files (16 resources) each returned HTTP 200 and matched their Git commit blobs byte for byte. The working Windows checkout differs only by Git-managed line endings in text files.

## Publication scope

Only the static website, optimised photographic assets, fonts, credit/licence files and relevant documentation were committed. The public Git tree contains no PDF, student ID, screenshots, browser profiles, video or legacy SVG files. Candidate text was scanned for student IDs and common credential patterns before committing; no findings were detected. No real customer records or payment details are included.

## Limits

Testing used Chromium with desktop, tablet and mobile viewport emulation from 320 to 1440 pixels. Safari, Firefox, real mobile hardware, real payments and backend services were not tested or claimed. Reservations are simulated and remain in each visitor’s browser. The verification did not change the user’s existing browser bookings. Subsequent documentation-only commits retain the tested website bytes.

## Future updates

See DEPLOYMENT.md. Review changes, stage only intended files, commit and push to `main`, then wait for Pages deployment and verify the public URL. Do not force-push.
