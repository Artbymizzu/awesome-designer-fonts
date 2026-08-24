# Font Data Guide

`fonts.json` is the source of truth for the collection. Add or update font
metadata there instead of editing generated lists directly.

## Fields

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | Yes | Official typeface name |
| `designer` | string | Yes | Designer or foundry |
| `category` | string | Yes | `Sans Serif`, `Serif`, `Display`, or `Monospace` |
| `description` | string | Yes | One concise, factual sentence |
| `recommendedFor` | string[] | Yes | Specific design scenarios |
| `tags` | string[] | Yes | Short discovery and filtering terms |
| `license.name` | string | Yes | Human-readable license name |
| `license.id` | string | Yes | SPDX identifier when one exists |
| `license.url` | URL | Yes | Authoritative license page |
| `license.access` | string | Yes | `Free`, `Paid`, or `Restricted` |
| `license.notes` | string | Yes | Concise commercial-use conditions |
| `commercial` | boolean | Yes | Whether general commercial use is available under the stated license |
| `variable` | boolean | Yes | Whether an official variable font is available |
| `download` | URL | Yes | Official specimen, download, or authorized purchase page |
| `preview.url` | URL or path | Yes | Official or authorized specimen image, or a local preview rendered from an official font file |
| `preview.source` | URL | Yes | Page that publishes the specimen image |
| `similarFonts` | string[] | Yes | Related typefaces for comparison |
| `lastVerified` | date | Yes | Date the attribution and license were checked |

## Entry Rules

- Use the official typeface spelling and designer or foundry attribution.
- Link to an official source or authorized retailer, never a font-file mirror.
- Use preview images published by the creator, foundry, official project, or authorized retailer.
- Verify license information against the official source.
- Distinguish fonts that are free to use from fonts that require a paid license.
- Use `Restricted` when a font is viewable or downloadable but not licensed for general third-party use.
- Treat `commercial: true` as permission under the stated terms, not as free use.
- Keep recommendations practical and descriptions factual.
- Use JSON booleans (`true` or `false`), not `Yes` or `No` strings.
- Keep entries sorted alphabetically by `name` within the data file.
