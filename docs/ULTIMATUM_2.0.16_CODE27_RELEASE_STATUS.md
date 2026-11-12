# Ultimatum 2.0.16 / code 27 - release build status

Date: 2026-11-12
Package: `com.ultimatum.flashshare`
Release focus: QR Easy Connect between Android and Windows Companion.

## Current verified state
- QR V1 source patch: 8/8 source file SHA256 matches on the developer's local PC.
- Previous Android release APK build: PASS; Windows QR Companion build: PASS; Windows QR installer build: PASS.
- The previous 2.0.16 release command failed AFTER Android compilation, in its APK certificate output parser. The Gradle version settings were rolled back to 2.0.15/code26.
- A corrected final-release build script was prepared and needs execution on the local Windows PC with the original signing key.
- A signed 2.0.16/code27 APK and AAB are not yet independently confirmed by this document.
- The installed Windows Companion and public Windows GitHub release are unchanged.

## Required release sequence
1. Rebuild 2.0.16/code27 from the SHA256-verified QR source using the original signing key.
2. Validate APK with Android apksigner; validate AAB with jarsigner and keytool; confirm identical expected upload certificates, AAB structure and SHA256.
3. Install the verified APK with `adb install -r` (data-preserving) on the connected authorized USB phone.
4. Pair Windows via **Pair by QR - Easy**, scan on Android, and approve using the green card.
5. Test both transfer directions, blocked/dismissed approval, QR expiry, reconnect and Find phone/manual fallback.
6. Verify that code27 is not already used on Google Play tracks. Upload signed AAB and any mapping file.
7. Only after real-device tests pass, publish the QR Windows installer as a distinct GitHub release and update the SHA256-gated download link on **both** Windows Companion pages. Add real Android/Windows screenshots.
8. Send users updated connection guidance after both compatible versions are available.

## Security and scope
Current PC Bridge uses HTTP over private LAN without transport TLS. The QR handoff sends a temporary code but local authorization data may traverse the LAN in plaintext. Use trusted networks only. Android's separate Phone Approval is still required. The Windows installer is not Authenticode-signed. Do not commit keystore files or tokens.

## Website typography
Use standard short hyphens (ASCII `-`) in visible release and setup text. Avoid typographic long dashes.

This document records build and publishing gates, not proof of Play Console approval or a live Windows update.
