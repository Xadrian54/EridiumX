# EridiumX

**v0.20.2** Desktop tools for encryption, passwords, authenticator codes and local file transfers, with optional Secure Share integration and a customizable workspace.

Application source is maintained privately. This repository provides public release packages and documentation. `SecureExtended` remains the internal name in some paths and formats.

## Getting started

Download your platform package from [Releases](https://github.com/Xadrian54/EridiumX/releases), extract the entire archive and keep the bundled runtime and libraries together.

| Platform | Launch |
| --- | --- |
| Windows x64 | Run the included executable. |
| Linux x64 | Run the included launcher. |
| macOS Apple silicon | Open the included app. |

Keep a separate copy of existing vaults before upgrading. Local tools work offline. Server workflows require a compatible HTTPS Secure Share.

Tab shortcuts
- Press Ctrl+K to open an area in the main window or Ctrl+Shift+K to open it in a separate window. Both shortcuts include hidden areas.
- To pop out a tab, hold the right mouse button, drag the tab above the tab bar, and release. With the left mouse button, hold for about 0.7 seconds before dragging out.

## Tools

| Area | Features |
| --- | --- |
| File / Text | Encrypt and decrypt files or text, optional ZIP compression, password generation with a saved length from 20 to 32 characters. |
| OpenPGP / Identities | Generate and manage keys, inspect fingerprints, encrypt, decrypt, sign, verify and re-encrypt supported content for another recipient. |
| Password generator | Character passwords or word passphrases, configurable character sets, and direct transfer to supported tools including QR generation. |
| Password manager | Encrypted local vaults, logins, notes, entry counts, password history, audit and additionally protected cards with optional IBAN/BIC. |
| Authenticator | TOTP in a standalone encrypted file or a separately protected vault section, QR/setup import and timed locking. |
| Vault sync | Optional bidirectional encrypted sync, offline-change detection, explicit conflict handling and bounded server backups. |
| Secure Share | Inspect metadata, retrieve encrypted content and forward supported encrypted containers unchanged to a local device. |
| Quick Share | Browser-based QR/NFC exchanges and native app reception, bounded collection counts and file expiry. Forward downloads to LocalSend or relay local receptions into an existing Quick exchange. |
| LocalSend | Local network discovery, manual IP entry, file selection, HTTPS transfer, progress and cancellation. Compatible with [LocalSend: Transfer Files](https://play.google.com/store/apps/details?id=org.localsend.localsend_app). |
| Rooms / Voice / Party | Encrypted Rooms, automatic updates, unread indication and access to voice and browser Watchparty workflows with cinema view and optional chat. |
| QR / Barcodes | Read codes, design QR content, generate/show/copy passwords and export PNG or SVG. |
| Recovery | Masks, dictionaries, typo variations and remembered characters with optional positions, with resumable searches for supported encryption profiles. |
| Convert | Images to PDF with page ordering, and Office to PDF through an installed LibreOffice instance. |
| Shredder | Overwrite selected files with configurable patterns and pacing. |
| Color Tool | Independent color selection and copyable HEX/RGB/sRGB output, including conversion of Display P3 input to sRGB. |
| Design / Settings | Visual theme editing, individual category accents, configuration import/export, reorderable areas and separate windows. |

## Storage and synchronization

Vaults use Argon2id and authenticated AES-256-GCM encryption. Local saves retain the preceding revision in an encrypted `.bak` file. Server sync and backups require the matching backup extension and explicit session approval. Keep the server address, backup ID and dedicated token accessible outside the vault.

The server applies a 64-snapshot retention policy alongside storage quotas. Restore a selected snapshot with its corresponding master password. Conflicting vault versions require a decision rather than silent replacement.

LocalSend works over a shared local network, including a suitable hotspot. Enable encryption in the companion app. Quick relay files are staged encrypted on disk, with bounded memory and cleanup. Passing an encrypted container unchanged requires a compatible decryption tool on the receiving device.

## Personalization

Use **Design / Settings** to edit colors, font size and rounding, import/export `.properties` files, and arrange areas. **Areas show/hide** beside Reset provides quick access to visibility and window controls. Closing a separate area window docks it again. Areas start docked after an app restart. Hiding Password Manager or Authenticator locks its session.

Settings export excludes passwords, tokens, vault contents and server permissions, but can contain device names and folder paths. Imported themes apply immediately, imported operating preferences after restart. Display P3 colors outside sRGB are clipped after confirmation.

## Notes

Office conversion requires a local LibreOffice installation. Recovery compatibility depends on the encryption profile, and unencrypted recovery checkpoints contain search inputs. File overwriting cannot remove copies retained by SSD wear levelling, snapshots or backups.

For problem reports, include the version, operating system, affected workflow, error and reproduction steps. Remove passwords, keys, authenticator seeds and personal data.

[Project website](https://eridium.xyz)
