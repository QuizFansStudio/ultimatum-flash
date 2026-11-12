# Ultimatum Windows Companion v1.1.0 - QR Easy Connect and Rich Preview

Release target: `windows-companion-v1.1.0`
Repository: `QuizFansStudio/ultimatum-flash`
Installer asset: `UltimatumCompanionSetup.exe`
Installer SHA-256: `B9F596C13599F1D20A3C97C11A8C5156F1FEB4D886D4194E91E45833CEE6DC0D`
Windows GUI SHA-256: `2AD1FEE1745A643104B2E52D3CBB2732714C3D0AF91DEC83A66F98318F1CD90C`

## Tested and reported by owner
- Windows build and installer build PASS from 2026-11-12 local log.
- Installed Windows GUI hash matches the final Windows QR and preview build.
- Owner confirmed QR scanning and pairing working in practice.
- Android 2.0.16 / versionCode 27 APK and AAB were generated with original signing certificate.
- Android AAB SHA-256: `D13F086F20EDEE5D85C22D3B21AD86B3C9D144A60B620D28B9D1AD44EBA850F5`.
- Individual file-type preview smoke tests have not been independently logged here. Do not treat compilation alone as proof of all media codecs/viewers.

## New Windows features
- QR shown on Windows using Pair by QR - Easy; Android 2.0.16+ scans it and still requires Approve & Connect.
- Existing Find phone and manual link fallback retained.
- In-app photo, text, DOCX text-only, and supported media preview.
- PDF, XLSX, PPTX open in the user-confirmed Windows associated viewer.
- Preview size limits and local temporary file cleanup apply.
- Existing transfer directions and Android-enforced Pro permissions remain.

## Official site routing
- https://quizfansstudio.github.io/UltimatumShare/windows.html
- https://flirtyquizcontact-rgb.github.io/UltimatumShare/windows.html

Both pages prefer new v1.1.0 only when GitHub reports the public release asset with the exact SHA-256 above. Otherwise, they identify the old v1.0.0 download as legacy without QR pairing.

## Security and publishing
- Windows installer is not Authenticode-signed. Explain the unknown publisher warning.
- Android PC Bridge uses local HTTP without TLS. Use a trusted private LAN only.
- Do not expose a PC Bridge port to the Internet.
- Do not upload private keystores or source credentials to GitHub.
- New release publication requires uploading the **exact verified installer from the owner's local computer**. No binary was uploaded merely by editing the websites or this document.
- Android AAB upload and Play review status are separate; only the owner can confirm their Play Console state.
