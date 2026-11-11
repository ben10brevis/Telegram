# NavGram

<p align="center"><img src="assets/branding/navgram-logo.svg" alt="NavGram Liquid Glass logo" width="180" /></p>

**NavGram** is an independent, community-built Android messaging client based on the Telegram Android source, with a custom iOS-inspired Liquid Glass visual direction.

> NavGram is an unofficial third-party client. It is not affiliated with, endorsed by, or supported by Telegram. Telegram is a trademark of its respective owner.

## Identity

- App name: **NavGram**
- Android application ID: `com.navgram.android`
- Debug application ID: `com.navgram.android.beta`
- Standalone application ID: `com.navgram.android.web`
- Visual direction: clear Liquid Glass, soft cyan/blue highlights and a custom NavGram mark.

## Builds

The existing GitHub Actions workflow builds a debug APK and uploads it as a workflow artifact. Workflow artifacts are temporary build outputs, not permanent releases.

Open **Actions → Build APK → Run workflow** to start a debug build. Download the APK from the completed run's Artifacts section.

A signed public release APK requires the project maintainer's own signing keystore and credentials. Never publish or reuse the upstream dummy keystore. Configure the signing secrets before enabling release distribution.

## Required project configuration

Before distributing builds, the maintainer must:

1. Obtain and use their own Telegram API `api_id` and `api_hash`: https://core.telegram.org/api/obtaining_api_id
2. Configure Firebase for the NavGram application IDs and supply a project-owned `google-services.json`.
3. Configure a project-owned Google Maps API key with appropriate package and signing-certificate restrictions.
4. Generate a private release keystore and store it securely. Keep keystore files and passwords out of Git.
5. Verify privacy disclosures, permissions, security practices and the app's complete source/build instructions.

The workflow expects `TG_APP_ID` and `TG_APP_HASH` repository Actions secrets for the Telegram API credentials.

## Upstream and licensing

NavGram is based on the Telegram for Android source: https://github.com/DrKLO/Telegram

This repository retains the upstream license and notices. Review the applicable source, dependency and asset licenses before distributing modified binaries. Publish the corresponding source for every distributed build as required by the applicable licenses.

## Disclaimer

NavGram is an independent client project. It does not represent itself as the official Telegram application, and it does not use Telegram's standard paper-plane launcher mark as its app identity.
