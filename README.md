# EridiumX

**NOTE:** The source code is reserved for the developers. However, the app contains the code up to the latest release, which is also available privately.


**v0.18.5** Desktop tools for file encryption, passwords, authenticator codes and document conversion, with Secure Share integration for encrypted transfers and Rooms.

Local tools work offline. Secure Share features require a compatible server. `SecureExtended` remains the internal project name in source paths, file formats and some release assets.

## Getting started

Download the package for your platform from **Releases**.

| Package | Launch |
| --- | --- |
| Linux x64 portable ZIP | Extract the entire archive and run the included launcher. |
| macOS Apple silicon (ARM64) portable ZIP | Extract the entire archive and open the included app. |
| Windows x64 portable ZIP | Extract the entire archive and run the included executable. Keep the bundled runtime and libraries together. |

Keep a separate copy of an existing vault before upgrading. Saving with a newer version may update its format.

## Features

| Tool | Capabilities |
| --- | --- |
| **File / Text** | Password-based encryption and decryption of files and text, with optional ZIP compression in supported workflows. |
| **OpenPGP** | Generate identities, inspect fingerprints, import and export keys, encrypt, decrypt, sign and verify text or files. |
| **Identities / Re-encryption** | Inspect HPKE and OpenPGP identities, export public keys and re-encrypt supported text for another recipient. |
| **Password generator** | Random character passwords, defaulting to 20 characters, or word passphrases. Configure character groups and exclusions, then transfer results directly to supported tools. |
| **Password manager** | Local encrypted vaults for logins and notes, entry counts, timestamps, up to two previous passwords per login and a local password audit. |
| **Authenticator** | TOTP codes in a standalone encrypted file or a separately protected section inside a vault. Import setup URIs, seeds or QR images and optionally lock sessions on a timer. |
| **Secure Share** | Inspect share metadata and retrieve encrypted text or files from a compatible HTTPS server. |
| **Quick Share** | Create a QR invitation in the server panel and send multiple files from a smartphone browser to a PC, with encrypted uploads and progress feedback. |
| **Rooms / Voice / Party** | Encrypted Rooms, contact invitations and access to voice and Watchparty workflows. The browser Watchparty includes YouTube link preview, chat search, date filtering and playback diagnostics. |
| **QR / Barcodes** | Read codes from images, clipboard or screen selections. Create customized QR codes and export PNG or SVG, including password-protected QR content. |
| **Recovery** | Local password recovery using masks, dictionaries, typo variations or remembered characters with optional positions. The remembered-character mode supports lengths up to 32 characters. |
| **Convert** | Combine images into one PDF, adjust page order and fit each image to portrait or landscape A4. Export Office documents to PDF through an installed LibreOffice instance. |
| **Shredder** | Overwrite selected files using configurable patterns and pacing. |

## Vault storage and backups

Vaults use Argon2id and authenticated AES-256-GCM encryption. Local saves retain the preceding revision in an encrypted `.bak` file.

Server backups require the **Secure Share backup extension** and explicit approval for the current vault session. Upload manually or after successful local saves. Restore a confirmed snapshot using its original master password, with verification and decryption performed locally.

Keep the server address, backup ID and dedicated token accessible outside the vault. Updated servers automatically thin older snapshots and enforce retention and storage limits.

## Conversion and recovery

Image-to-PDF conversion runs locally. For Office-to-PDF conversion, select your LibreOffice executable (`soffice.exe` or `soffice`). 
It runs in the background for the conversion.

Recovery supports selected SecureExtended containers, identities and vaults, OpenPGP files, ZIP and 7z archives, encrypted Office and LibreOffice documents, and PDFs. Compatibility depends on the encryption profile. Checkpoints allow searches to resume later, but unencrypted checkpoints contain the search inputs.

File overwriting cannot remove copies retained by SSD wear levelling, snapshots or backups.

## Reporting a problem

Include the app version, operating system, affected workflow, error message and reproduction steps. For JAR launches, include the Java version. Remove passwords, private keys, authenticator seeds and personal data from reports.

[Project website](https://eridium.xyz)
