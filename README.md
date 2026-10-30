# Black Friday Finder (Android)

A Kotlin + Jetpack Compose Android starter app for a UK Black Friday deal-discovery product.

## Included and working
- Android app shell with dark/gold UI
- Deal list, category chips and text search
- Deal detail screen with retailer link-out
- Save/remove favourites for the current app session
- Premium feature/paywall preview screen
- GBP price display and estimated percentage saving

## Important prototype limitations
The included offers are **sample/demo data**, not live retailer offers. The retailer links are generic destinations, not product-specific affiliate links. Favourites are held in app memory and reset when the process is killed. Premium is a feature preview only; no payment is taken and no subscription is activated.

## Open in Android Studio
1. Install the current Android Studio and Android SDK (API 35).
2. Open this folder as a project.
3. Allow Gradle sync and install on an Android device/emulator.

This environment did not have the Android SDK or Gradle installed, so an APK could not be compiled here.

## Required before a public launch
1. Connect a legitimate deals data source (retailer affiliate feeds/APIs or an approved product-data provider). Do not scrape sites in breach of their terms.
2. Add a backend/API that normalises retailer, product, current price, previous price, currency, stock, timestamp and affiliate URL.
3. Store user accounts, saved deals and alert preferences securely (for example, Firebase or your own backend).
4. Implement price history from timestamped observations; never label a discount as genuine without a reliable reference price.
5. Add Firebase Cloud Messaging or another push provider for alerts.
6. Add Google Play Billing subscriptions and server-side purchase verification. Premium access must be granted only after verified purchase and revoked/updated from subscription status.
7. Add privacy policy, terms, data deletion, consent and UK GDPR compliance.
8. Test retailer links, pricing accuracy, accessibility, crashes and Play Store requirements.

## Suggested premium setup
Requested premium price: £1.99/month. This is a pricing requirement only; Google Play Billing is not connected and no subscription product has been created or activated.

## Build an APK using GitHub from an Android phone (no PC required)
1. Create a GitHub account if you do not already have one.
2. In GitHub, create a new repository named `BlackFridayFinder`.
3. Upload the contents of this project ZIP to the repository (make sure the `.github/workflows/build-apk.yml` file is included).
4. Open the repository's **Actions** tab and select **Build Android APK**. If prompted, enable Actions, then choose **Run workflow**.
5. When the run finishes successfully, open that run and download the artifact named `Black-Friday-Finder-debug-apk`.
6. Extract the downloaded artifact and install `app-debug.apk` on your Android device. If Android asks, allow Chrome or Files to install unknown apps.

This produces a debug APK for testing/sideloading, not a Play Store release-signed APK. The app still contains demo deals and does not yet have live retailer feeds or working £1.99/month billing.
