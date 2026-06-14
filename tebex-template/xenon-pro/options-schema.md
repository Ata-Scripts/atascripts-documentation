# Options - Schema

## Configuration Reference

This page covers every setting available in your XENON-PRO store template. All settings are managed through the **Tebex dashboard → Store → Appearance → Edit Template → Settings** panel.

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

***

### Table of Contents

1. SEO
2. Links
3. General
4. Footer
5. Hero
6. Customer Feedbacks
7. Cards
8. Stats Modules
9. FAQ
10. Subscription Benefits Section
11. Discount Announce Module

***

### SEO

Controls the metadata that search engines and social platforms read when they index or share your store.

| Setting              | ID                 | Description                                                                                                                             |
| -------------------- | ------------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Meta Description** | `meta-description` | The short paragraph that appears under your store name in Google search results. Keep it between 120 - 160 characters for best results. |
| **Meta Keywords**    | `meta-keywords`    | A comma-separated list of keywords that describe your store. While less important for modern SEO, some platforms still read this field. |
| **OG Title**         | `og-title`         | The title shown when someone shares a link to your store on Discord, Twitter, or Facebook (Open Graph title).                           |

> **Tip:** Write your Meta Description as a clear, single sentence that tells a potential customer exactly what your store sells.

***

### Links

Social and external URLs that appear in the navigation bar and footer of your store.

| Setting            | ID               | Description                                                     |
| ------------------ | ---------------- | --------------------------------------------------------------- |
| **Discord Link**   | `link-discord`   | Your Discord server invite URL. Shown in the navbar and footer. |
| **FiveM Link**     | `link-fivem`     | Link to your FiveM server listing or CFX page.                  |
| **YouTube Link**   | `link-youtube`   | Your YouTube channel URL.                                       |
| **TikTok Link**    | `link-tiktok`    | Your TikTok profile URL.                                        |
| **Instagram Link** | `link-instagram` | Your Instagram profile URL.                                     |
| **Gitbook Link**   | `link-gitbook`   | Link to your documentation site (GitBook or any docs URL).      |

> Any link left as the placeholder default will still render in the UI. Set unused links to `#` or contact support if you want to hide a specific icon.

***

### General

Core appearance and behaviour settings that affect the entire store.

| Setting                   | ID                     | Type   | Description                                                                                                                        |
| ------------------------- | ---------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Enable Tag Filter**     | `enable-tag-filter`    | Toggle | Shows or hides the tag filter bar on category pages. When enabled, customers can filter packages by tags you've assigned in Tebex. |
| **Store Slug**            | `store-slug`           | Text   | A short tagline shown in small text near the logo (e.g. `Powered by Tebex`). Think of it as a subtitle for your brand.             |
| **Primary Colour**        | `color-primary`        | Colour | The main accent colour used for buttons, highlights, and interactive elements. Default: `#FFB53D`.                                 |
| **Secondary Colour**      | `color-secondary`      | Colour | A slightly darker shade of the primary colour, used for hover states and gradients. Default: `#c58d32`.                            |
| **Dark Primary Colour**   | `dark-color-primary`   | Colour | The darkest background colour, used for the page body and hero section. Default: `#111114`.                                        |
| **Dark Secondary Colour** | `dark-color-secondary` | Colour | A slightly lighter dark tone, used for cards, modals, and panels. Default: `#16161A`.                                              |

> **Colour tip:** Primary and Secondary should be complementary shades of the same hue. Dark Primary and Dark Secondary should be near-black with a subtle difference in lightness.

***

### Footer

Customise the bottom section of every page - your disclaimer text, quick links, support email, and DMCA badge.

#### Disclaimer Text

| Setting             | ID                | Description                                                                                                                                           |
| ------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Under Logo Text** | `under-logo-text` | Small text displayed beneath your store logo in the footer. Typically used for a legal disclaimer (e.g. "We are not affiliated with Rockstar Games"). |

#### Footer Quick Links

You have **4 footer link slots**. Each slot has a URL and a display label.

| Setting                 | ID                   | Description                                                      |
| ----------------------- | -------------------- | ---------------------------------------------------------------- |
| **Footer Link URL #1**  | `link-footer-1-url`  | Full URL for quick link #1.                                      |
| **Footer Link Text #1** | `link-footer-1-text` | The clickable label for quick link #1 (e.g. `Terms of Service`). |
| **Footer Link URL #2**  | `link-footer-2-url`  | Full URL for quick link #2.                                      |
| **Footer Link Text #2** | `link-footer-2-text` | The clickable label for quick link #2.                           |
| **Footer Link URL #3**  | `link-footer-3-url`  | Full URL for quick link #3.                                      |
| **Footer Link Text #3** | `link-footer-3-text` | The clickable label for quick link #3.                           |
| **Footer Link URL #4**  | `link-footer-4-url`  | Full URL for quick link #4.                                      |
| **Footer Link Text #4** | `link-footer-4-text` | The clickable label for quick link #4.                           |

#### Support & Legal

| Setting           | ID              | Description                                                                     |
| ----------------- | --------------- | ------------------------------------------------------------------------------- |
| **Email Support** | `email-support` | Your support email address, shown as a clickable `mailto:` link in the footer.  |
| **DMCA Image**    | `dmca-image`    | Upload your DMCA badge image. This is displayed as a small badge in the footer. |
| **DMCA Link**     | `dmca-link`     | The URL the DMCA badge links to (typically your DMCA takedown policy page).     |

***

### Hero

The large banner section at the top of your homepage - the first thing every visitor sees.

#### Background & Text

| Setting                | ID                 | Description                                                                                                                                 |
| ---------------------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Hero Section Image** | `hero-image`       | The decorative image displayed on the right side of the hero banner. Best results with a transparent PNG or a dark-background image.        |
| **Hero Description**   | `hero-description` | The subtitle paragraph below your store name in the hero. Keep it concise - 1 to 2 sentences.                                               |
| **Hero Announce**      | `hero-announce`    | A small pill-shaped badge shown above the main heading. Use it for seasonal announcements, sales, or news (e.g. `🎉 Summer Sale is live!`). |

#### Hero Buttons

You have **2 customisable CTA buttons** in the hero section.

**Button 1 (Primary - "Play" by default)**

| Setting    | ID                     | Description                                                       |
| ---------- | ---------------------- | ----------------------------------------------------------------- |
| **Enable** | `hero-button-1-enable` | Show or hide this button.                                         |
| **Icon**   | `hero-button-1-icon`   | Font Awesome class for the button icon (e.g. `fa-solid fa-play`). |
| **Text**   | `hero-button-1-text`   | The label on the button (e.g. `Play Now`).                        |
| **URL**    | `hero-button-1-url`    | Where the button takes the user when clicked.                     |

**Button 2 (Secondary - "Discord" by default)**

| Setting    | ID                     | Description                                                           |
| ---------- | ---------------------- | --------------------------------------------------------------------- |
| **Enable** | `hero-button-2-enable` | Show or hide this button.                                             |
| **Icon**   | `hero-button-2-icon`   | Font Awesome class for the button icon (e.g. `fa-brands fa-discord`). |
| **Text**   | `hero-button-2-text`   | The label on the button (e.g. `Join Discord`).                        |
| **URL**    | `hero-button-2-url`    | Where the button takes the user when clicked.                         |

> **Icon tip:** Find icon class names at [fontawesome.com/icons](https://fontawesome.com/icons). The template loads Font Awesome 7 Free, so use `fa-solid`, `fa-regular`, or `fa-brands` prefixes.

***

### Customer Feedbacks

A testimonials/reviews carousel on the homepage. You can configure **3 customer feedback cards**.

Each card has the following fields (replace `N` with `1`, `2`, or `3`):

| Setting             | ID                    | Description                                                                 |
| ------------------- | --------------------- | --------------------------------------------------------------------------- |
| **Name**            | `feedback-N-name`     | The customer's display name (e.g. `John Doe`).                              |
| **Role**            | `feedback-N-role`     | A short label shown under the name (e.g. `Server Owner`, `Verified Buyer`). |
| **Rating**          | `feedback-N-rating`   | Star rating from `0` to `5`. Renders as filled stars on the card.           |
| **Profile Picture** | `feedback-N-profile`  | Upload or link a profile photo for the reviewer. Square images work best.   |
| **Feedback Text**   | `feedback-N-feedback` | The actual review text shown on the card.                                   |

> Keep feedback text between 1–3 sentences for a clean card layout.

***

### Cards

Three feature/highlight cards shown in a row on the homepage. Use these to showcase your most popular script categories, key features, or unique selling points.

Each card has the following fields (replace `N` with `1`, `2`, or `3`):

| Setting         | ID                   | Description                                                    |
| --------------- | -------------------- | -------------------------------------------------------------- |
| **Icon**        | `card-N-icon`        | Font Awesome class for the card icon (e.g. `fa-solid fa-car`). |
| **Title**       | `card-N-title`       | Short heading for the card (e.g. `Vehicle Scripts`).           |
| **Description** | `card-N-description` | A brief sentence explaining what this card represents.         |

***

### Stats Modules

Three animated counter boxes that count up when scrolled into view on the homepage. Use them to display social proof numbers.

Each stat has a title and a numeric value (replace `N` with `1`, `2`, or `3`):

| Setting   | ID                     | Description                                                                        |
| --------- | ---------------------- | ---------------------------------------------------------------------------------- |
| **Title** | `stats-module-N-title` | Label above the number (e.g. `Total Sales`, `Happy Customers`).                    |
| **Value** | `stats-module-N-value` | The number to count up to. Enter digits only, no commas or symbols (e.g. `51200`). |

> The counter animation triggers once when the stats section enters the viewport. The number formats automatically with locale-aware separators.

***

### FAQ

Up to **8 frequently asked questions** displayed in an accordion on your store. Customers can expand each question to read the answer.

Each FAQ entry has a question and an answer (replace `N` with `1` through `8`):

| Setting      | ID               | Description                                                                     |
| ------------ | ---------------- | ------------------------------------------------------------------------------- |
| **Question** | `faq-N-question` | The question text shown in the collapsed accordion header.                      |
| **Answer**   | `faq-N-answer`   | The full answer shown when the question is expanded. Plain text only - no HTML. |

> **Best practice:** Order FAQs from most-asked to least-asked. Common topics: refunds, how downloads work, escrow, payment methods, reselling policy.

***

### Subscription Benefits Section

This section appears on **tiered subscription category pages** only (`category.tiered.html`). It displays a 3-column grid of 6 benefit cards explaining why customers should subscribe.

Each box has an icon, title, and description (replace `N` with `1` through `6`):

| Setting         | ID                | Description                                                                                                                     |
| --------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **Icon Class**  | `sub-box-N-icon`  | Font Awesome class for the box icon (e.g. `fas fa-bolt`). The icon is automatically coloured to match each box's accent colour. |
| **Title**       | `sub-box-N-title` | Short heading for the benefit (e.g. `Instant Access`, `Priority Support`).                                                      |
| **Description** | `sub-box-N-desc`  | One or two sentences explaining the benefit in detail.                                                                          |

#### Default Icons per Box

| Box | Default Icon       | Default Title     |
| --- | ------------------ | ----------------- |
| 1   | `fas fa-bolt`      | Instant Access    |
| 2   | `fas fa-tag`       | Exclusive Pricing |
| 3   | `fas fa-sync-alt`  | Always Up to Date |
| 4   | `fas fa-headset`   | Priority Support  |
| 5   | `fas fa-lock-open` | No Lock-In        |
| 6   | `fas fa-star`      | Premium Quality   |

> This section only renders on pages that use the tiered category template. It will not appear on standard category pages.

***

### Discount Announce Module

A dismissible announcement bar that appears at the **very top of every page**, above the navigation. Use it to promote discount codes, limited-time sales, or important announcements.

| Setting               | ID                                     | Type   | Description                                                                                                                                          |
| --------------------- | -------------------------------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Enable Module**     | `enable-discount-bar-module`           | Toggle | Show or hide the announcement bar site-wide.                                                                                                         |
| **Announcement Text** | `discount-bar-module-text`             | Text   | The main message in the bar. Supports basic HTML tags - use `<strong>` to bold the discount amount (e.g. `Get <strong>20% OFF</strong> with code:`). |
| **Discount Code**     | `discount-bar-module-code`             | Text   | The promo code displayed next to the announcement text. Customers can click it to copy to clipboard.                                                 |
| **Re-show Wait Time** | `wait-time-discount-bar-module`        | Select | How long (in minutes) before the bar reappears after a customer closes it. Options: `15`, `30`, `60`, `120`, `180`, or `custom`.                     |
| **Custom Wait Time**  | `wait-time-discount-bar-module-custom` | Text   | Only active when the wait time above is set to `custom`. Enter a value in minutes (e.g. `2880` = 2 days, `10080` = 1 week).                          |
| **Can Be Closed**     | `can-close-discount-bar`               | Toggle | When `true`, a close (×) button appears so customers can dismiss the bar. When `false`, the bar is permanently visible with no way to close it.      |

> **Re-show logic:** The close timestamp is stored in the browser's `localStorage`. Clearing browser data or using a different device will cause the bar to reappear regardless of the wait time.
