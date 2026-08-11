# TrueMargin — Etsy Profit & Fee Calculator Chrome Extension

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Tests](https://img.shields.io/badge/tests-73%20passing-brightgreen.svg)
![Manifest](https://img.shields.io/badge/manifest-V3-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

**TrueMargin** is a lightweight, high-precision Google Chrome Extension designed for Etsy sellers to calculate exact net margins, taxes, and hidden platform fees directly on listing pages.

---

## Key Capabilities & Business Logic

- **Comprehensive Fee Breakdown:** Calculates Listing ($0.20), Transaction (6.5%), Payment Processing, and Onsite/Offsite Ads (12%/15%).
- **Tax-Adjusted Processing Base:** Accurately models the US Sales Tax impact on Payment Processing fee calculations per Etsy Payments Policy.
- **Regional Regulatory Operating Fees:** Out-of-the-box support for country-specific regulatory rates (UK 0.48%, FR 1.14%, ES 0.88%, HU 1.97%, CA 0.50%, IT 0.80%, etc.).
- **Service VAT & Exemption Engine:** Per-item line VAT calculation with EU B2B VAT ID exemption profile capability (`vatExempt`).
- **Dynamic FX & Buffer System:** Currency conversion modeling with standard 2.5% FX spread and outdated rate warnings (`fx.stale`).
- **70+ Automated Unit Tests:** Core calculation algorithms are strictly covered against floating-point edge cases and multi-quantity item semantics.

---

## Architectural Scope & Transparency

TrueMargin is engineered specifically for **item-level unit economics**. 

> **Important Note:** Item-level calculators do not account for shop-wide overheads such as unsold listing auto-renewals ($0.20 per 4 months) or Etsy Plus monthly subscriptions. These must be evaluated at the store level.

---

## Privacy & Security

- **Zero Telemetry:** No analytics scripts, no tracking pixels, zero external data storage.
- **Local Execution:** DOM parsing and math calculations execute entirely within the client's browser context.

---

## Installation

### Official Store Release
Download directly from the [Chrome Web Store](#) *(Link coming upon review completion)*.

### Developer Build (Manual Setup)
1. Clone this repository: `git clone https://github.com/YOUR_USERNAME/truemargin-extension.git`
2. Open Chrome and navigate to `chrome://extensions/`
3. Enable **Developer mode** in the top right corner.
4. Click **Load unpacked** and select the root directory of this repository.

---

## Tech Stack & Testing

- **Manifest V3**
- **JavaScript (ES6+)**
- **Vitest** for unit test suite execution (`npm test`)

---

## License

Distributed under the MIT License.
