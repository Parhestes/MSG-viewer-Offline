# MSG Viewer

Browser-based Outlook `.msg` file reader. No installation required — just a single HTML file.

## Features

- **HTML body rendering** — Displays the original Outlook formatting (fonts, tables, colors, signatures) as-is
- **Attachment management** — Lists all attachments, previews images inline, one-click download
- **Outlook-style layout** — Familiar envelope UI with sender, recipients, date, and subject
- **Header inspection** — Full email headers with syntax highlighting
- **Multi-file support** — Open multiple `.msg` files at once and switch between them
- **Privacy-first** — Everything runs locally in your browser, no data is sent anywhere

## Usage

1. Download `msg-viewer.html`
2. Open it in any browser (Safari, Chrome, Firefox)
3. Drag & drop your `.msg` file or click to browse

## Why?

Opening Outlook `.msg` files on macOS typically requires installing Microsoft Outlook or relying on subpar App Store alternatives. This tool solves it with a single HTML file — no installation, no account, no internet connection needed.

## Technical Details

- Parses OLE2/CFBF format using the [msgreader](https://www.npmjs.com/package/msgreader) library
- Patched to extract `0x1013` (PidTagBodyHtml) for original HTML body rendering
- Plain text fallback with automatic paragraph, signature, and disclaimer detection

## License

MIT
