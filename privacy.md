# Privacy Policy for Retire Roadmap

**Effective date:** 13 JUNE 2026  
**Contact:** heylonstudio@gmail.com

This privacy policy describes how the Retire Roadmap mobile application ("Retire Roadmap", "the app", "we", "our") handles your information. Retire Roadmap is a retirement planning and financial projection tool distributed via the Apple App Store and Google Play.

We have intentionally designed Retire Roadmap to keep your financial inputs on your device wherever possible. Portfolio entries, planning settings, and generated projections are stored locally and computed on your device. We do not operate servers that receive or store your retirement plan details.

---

## 1. Information stored and processed on your device

Retire Roadmap lets you build a retirement roadmap by entering assets, spending assumptions, inflation, growth rates, withdrawal strategies, and related settings. This information is used only to run projections and display charts and tables in the app:

- **Portfolio and settings** — assets (stocks, crypto, custom lines such as savings or pension income), retirement year, annual lifestyle spending, inflation, planning horizon, currency preference, and withdrawal strategy are saved on the device using local storage (SharedPreferences).

- **Projections** — year-by-year balances, charts, sensitivity views, and export files (PDF, Excel, or shared text) are generated on the device from your inputs.

- **Optional API key (advanced)** — if you choose to add a personal Finnhub API key in Advanced Settings, it is stored only on your device and used only as an optional backup when automatic stock price refresh needs it. Most users never need to add a key.

We do not copy, upload, transmit, or store your portfolio details, scenario names, or projection results on any server operated by us.

When you use **Export** or **Share**, you choose the destination (email, cloud drive, messaging app, etc.) through your operating system's share sheet. We do not receive a copy of exported files unless you send them to us directly (for example by email for support).

---

## 2. Information collected by third-party services

Retire Roadmap integrates third-party services for advertising, subscription payments, market data, exchange rates, and store distribution. These services may collect limited information as described below.

### a. Advertising — Google AdMob

Retire Roadmap uses Google AdMob in the free version. A **banner ad** may appear at the bottom of the main screen while you use the app. Premium subscribers are not shown banner ads through the app's own presentation logic.

Depending on device settings and Google's policies, ads may involve standard ad-related mechanisms (for example measurement or eligibility checks). AdMob may collect data such as advertising identifiers (for example AAID / IDFA where applicable), coarse location derived from IP address, device information (such as model and OS version), language/locale, and app or ad interaction events used to deliver and measure advertising. How Google handles such data is explained in [Google's Privacy Policy](https://policies.google.com/privacy).

Where your device or OS allows, you can limit ad personalisation or reset advertising identifiers — for example via your Google or Apple account and privacy settings (wording and menu paths vary by version).

Premium subscribers are not shown the banner advertising described above through Retire Roadmap's own presentation logic. The Google Mobile Ads SDK may still be included in the app binary and initialised during app startup (for example before or after your subscription status is known); we do not use it to show paid subscribers the free-tier banner ads.

### b. Subscriptions and purchases — RevenueCat

Retire Roadmap offers an optional **Premium** subscription (monthly and yearly) and a one-time **Lifetime** purchase. Payment processing is handled exclusively by the Apple App Store or Google Play. We never see your payment card or bank details.

To verify your subscription status across devices and sessions, we use RevenueCat, a third-party subscription management platform. When you make a purchase, RevenueCat receives:

- A pseudonymous, app-generated user identifier (it is not your name, email, or phone number).
- The purchase receipt issued by Apple or Google.
- Subscription status (active, expired, in grace period, etc.).
- Country code and the store-product identifier you purchased.

RevenueCat's privacy policy: [https://www.revenuecat.com/privacy/](https://www.revenuecat.com/privacy/)

We use this data only to determine whether your device should be treated as Premium and to honour restore-purchase requests as required by the App Store and Play Store.

### c. Market data and exchange rates

When you add a listed stock or crypto asset, tap **Fetch Latest Prices**, or when the app loads exchange rates for currency display, it contacts public third-party services over the internet. These requests are made **from your device** and are limited to what each service needs to return a quote or rate. We do not route your full portfolio through our own servers.

**Stock quotes** are fetched automatically — no account or API key is required from you. The app tries **Yahoo Finance** public market-data endpoints first, then **[Finnhub](https://finnhub.io/privacy-policy)** as a backup if the first source does not return a usable price. Yahoo requests send only the ticker symbol(s) you entered. Finnhub requests send the ticker symbol(s) and an API token (the app's built-in token, or your optional personal key stored on device if you added one).

Depending on which asset type you refresh, requests may go to:

| Purpose | Provider | What is sent (examples) |
|--------|----------|-------------------------|
| Stock quotes (primary) | Yahoo Finance ([Yahoo Privacy Policy](https://legal.yahoo.com/us/en/yahoo/privacy/index.html)) | Stock ticker symbol(s) derived from what you entered (for example `AAPL`, `TSLA`) |
| Stock quotes (backup) | [Finnhub](https://finnhub.io/privacy-policy) | Stock ticker symbol(s); an API token (the app's built-in default or your optional personal key stored on device) |
| Crypto quotes | [CoinGecko](https://www.coingecko.com/en/privacy) and/or [Binance](https://www.binance.com/en/privacy) | Cryptocurrency identifier or trading pair derived from the ticker you entered |
| Exchange rates | [ExchangeRate-API](https://www.exchangerate-api.com/privacy) | A request for USD-based FX rates (no portfolio payload) |

Those providers handle data under their own policies. They may log IP address, request metadata, and API usage in line with their terms. Yahoo Finance is accessed through public quote endpoints rather than a user-signup API product. Retire Roadmap does not send your asset labels, account numbers, or retirement spending amounts to these market-data services — only the symbols or identifiers needed to look up prices or rates.

### d. App distribution and updates — Apple, Google

When you install or update Retire Roadmap, Apple and/or Google collect installation and crash telemetry as part of their normal store operation. We do not control this collection. Their respective policies apply:

- Apple: [https://www.apple.com/legal/privacy/](https://www.apple.com/legal/privacy/)
- Google: [https://policies.google.com/privacy](https://policies.google.com/privacy)

On Android, the app may use Google Play's in-app update flow to prompt you when a newer version is available. That interaction is between your device and Google Play.

---

## 3. Information we do not collect

We do not collect or store your name, email address, phone number, postal address, or any account-style information. Retire Roadmap has no user accounts and no sign-in.

We do not upload your portfolio, scenarios, projections, or exports to any server operated by us.

We do not access your photo library, contacts, calendar, microphone, or precise GPS location.

We do not sell personal data to third parties.

---

## 4. Children's privacy

Retire Roadmap is intended for users 18 and older. We do not knowingly collect or solicit data from children under 13 (or under 16 in jurisdictions where that age applies). If you believe a child has used the app and provided data, please contact us at the email above and we will assist where possible.

---

## 5. Permissions and network access

Retire Roadmap will, depending on your operating system, request or use:

- **Internet access** — required to refresh market prices and exchange rates, load ads (free tier), verify subscriptions, and check for app updates on Android.

The app does not request photo library, camera, contacts, location, or notification permissions for marketing in the current release.

You can revoke network access in your device's system settings; without internet, price refresh, ads, subscription verification, and Play Store update prompts will not work as designed. Core projection math on data already on the device can still run offline.

---

## 6. Data retention and deletion

Because Retire Roadmap does not collect or store your portfolio or personal planning data on any server operated by us, there is nothing on our side to retain or delete for that information.

Data on your device remains until you clear app storage, uninstall the app, or use in-app reset options where available.

Subscription receipts retained by RevenueCat are kept for the duration required by Apple and Google's billing and tax obligations. If you would like the pseudonymous RevenueCat identifier associated with your purchases removed from RevenueCat's records, contact us at the email above and we will submit a deletion request to RevenueCat on your behalf.

---

## 7. Security

Network communication between Retire Roadmap and the third-party services listed above (AdMob, RevenueCat, Yahoo Finance, Finnhub, CoinGecko, Binance, ExchangeRate-API, Apple, Google) is encrypted in transit using HTTPS / TLS. Your portfolio and settings remain in your device's local app storage, protected by your device's operating-system security.

---

## 8. Changes to this policy

We may update this privacy policy from time to time, for example to reflect new third-party services or changes in regulation. The "Effective date" at the top of this document indicates when the latest version became active. Material changes will be announced in the app's release notes.

---

## 9. Support

For help with Retire Roadmap, contact: heylonstudio@gmail.com

---

## 10. Contact

Questions, requests, or complaints about this policy can be sent to: heylonstudio@gmail.com
