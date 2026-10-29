# AZoom Car Rental | ISIT207 Assignment 2

A responsive, front-end electric car rental prototype made with **HTML5, CSS3 and vanilla JavaScript**.

## Run the website

Open `index.html` in Chrome, Edge or Firefox. Alternatively run `python -m http.server 8000` in this folder and open http://localhost:8000.

## Features

- Responsive homepage, fleet cards, body type filter and price sorting.
- Date validation, 1-365 rental days, daily/weekly/monthly discounts and rental summary with 9% GST.
- Reservation with sample credit-card selection (no real card data entered or processed).
- Browser-local demo booking reference stored with `localStorage`.
- Manage booking through reference + email, including simulated collection, return, employee inspection (with damage charge) and final credit card payment.
- Clear steps, designated branch carparks, FAQs, labels and keyboard support.

## Demonstrate the rental journey

1. Select rental dates, click **Search cars**, and choose **Book now** for a vehicle.
2. Enter sample customer details, select City Hall or Marina Bay, review the estimated cost, then continue.
3. Tick the demo consent and confirm the reservation using one of the **sample cards**.
4. Select **View booking journey**. The reference and email should auto-fill.
5. Simulate office collection, carpark return, employee inspection (choose no damage or a damage option), and final credit card payment.
6. Refresh and use **Manage booking** to retrieve the saved example with its reference and email.

## Assumptions and limitations

- Branch names, fleet, rates and damage charges are illustrative assumptions, not real AZoom business information.
- The estimate uses daily price × rental days, with a 15% discount for 7–29 days or a 25% discount for 30+ days; 9% GST is applied to rental charges.
- Return is to the designated parking area of the selected pick-up branch.
- The credit-card confirmation is **a simulation only**; there are no card-number fields, real charges or payment gateway.
- Bookings live only in the current browser's `localStorage`. No staff login, server database, real inventory, authentication or payment processing is provided or claimed.
- A production site would require secure login, a booking API, payment gateway, database, inventory validation and official locations.

## Deploy (GitHub Pages)

1. Upload `index.html`, `style.css`, `script.js` and `assets/` to the root of a GitHub repository.
2. In the GitHub repository, open **Settings → Pages → Build and deployment**.
3. Choose **Deploy from a branch**, set branch `main` and folder `/ (root)`, then save.
4. Copy the public Pages URL into your report and test the booking process there.

## Coursework submission

- Share the website URL and your Google Drive source-code folder URL.
- Submit the PDF design review (maximum 5 pages) with screenshots and shared Google Drive screen-recording URL.
- Record a narrated demonstration; the parent package contains an earlier narrated draft video, which does not show the refreshed photographs. The website is live at https://leafyve.github.io/azoom-car-rental/ and was verified on 29 October 2026; see LIVE_VERIFICATION.md.
- Review UOW's guidance on acknowledging any AI-assisted content and adapt the work to reflect your own understanding.

## October 2026 visual refresh

- Real photographs of all six vehicle models and two Singapore landmarks, optimised as local WebP files.
- Custom AI-generated hero with responsive image sizes and a visible disclosure.
- Vehicle photos retain the complete frame. Location photographs are cropped to fill matching cards.
- Larger card and form text, consistent spacing, keyboard focus indicators, restrained hover feedback and mobile booking management.
- Existing rental prices, discounts, localStorage key and collection/return/inspection/payment transitions are preserved.
- Corrected the original phone-pattern syntax for modern browser validation.
- Fonts are self-hosted, so rendering does not require Google Fonts access.

Image sources, creators, licences and modifications: `assets/IMAGE_CREDITS.md` or the **Image credits** link in the footer. Full font licences are included in `assets/fonts/`.

See `TEST_RESULTS.md` for observed browser checks and `DEPLOYMENT.md` for exact GitHub Pages instructions. Local captures are in `screenshots/` and are intentionally excluded from Git. The five-page report is saved in the parent package directory, outside the public website folder.

## Repository and updates

Repository: https://github.com/Leafyve/azoom-car-rental

Live GitHub Pages website: https://leafyve.github.io/azoom-car-rental/

Publishing uses the `main` branch and repository root. See `DEPLOYMENT.md` for deployment status and future update commands. Private assignment reports, screenshots, temporary files and legacy SVG illustrations are excluded from Git.
