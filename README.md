# MetaMate-ai Docs
This public repository hosts documentation, screenshots and support links for the MetaMate AI plugin for Umbraco

# MetaMate AI

> AI-powered meta title and meta description generation for **Umbraco 17** — directly in the backoffice.

MetaMate AI helps editors and developers find pages with missing meta data and generate clean, relevant meta titles and descriptions from the **actual page content**.

---

## Why MetaMate AI?

MetaMate AI is intentionally focused.

It does **not** try to be a full SEO suite.
It does one job well:

- find missing meta title and meta description
- generate missing values with AI
- keep existing values intact
- stay predictable inside the normal Umbraco workflow

No clutter. No overwrite surprises. No giant SEO toolbox.

---

## Highlights

- Built for **Umbraco 17**
- Backoffice dashboard for settings, discovery, and bulk generation
- Single-page generate button directly in the document workspace
- Bulk generation for published pages under a selected root
- Generates from **real page content**
- Writes only to **empty** fields
- Never overwrites existing meta values
- Configurable model, language, temperature, source aliases, and document type filtering

---

## Features

### Single-page generate
Generate missing meta directly from the current document.

MetaMate AI:
- checks the current page
- generates only missing fields
- leaves existing values untouched
- saves and publishes when changes were made

### Find missing meta
Scan published pages under a selected root and list pages that are missing:
- meta title
- meta description
- or both

### Bulk generate
Generate missing meta in bulk for published pages below a selected root.

### Configurable source fields
Choose which property aliases MetaMate AI should read as source content.

Example:

```text
bodyText,mainContent,content,seoText
```

### Optional document type filtering
Restrict generation to specific Umbraco document types.

Example:

```text
articlePage,productPage,landingPage
```

Leave empty to include all document types.

---

## Requirements

- Umbraco CMS 17+
- OpenAI API key
- Existing properties for meta title and meta description on relevant document types

---

## Installation

Install via NuGet:

```bash
dotnet add package MetaMateAi
```

Then restart the site and open the **MetaMate AI** section in the Umbraco backoffice.

---

## Configuration

Configure MetaMate AI from the backoffice dashboard.

### OpenAI API key
Used for generation requests.

### Model
The AI model used for generating meta content.

### Language
Controls the language of generated output.

### Temperature
Controls how deterministic or creative the output should be.

### Title alias
The property alias used for the meta title field.

### Description alias
The property alias used for the meta description field.

### Source aliases (csv)
Comma-separated list of property aliases that MetaMate AI can read from when generating meta text.

### Allowed document types (csv)
Comma-separated list of Umbraco document type aliases that MetaMate AI is allowed to run on.

Leave empty to allow all document types.

---

## How it works

MetaMate AI reads text from the configured source fields on the page.

It then generates:
- a meta title
- a meta description

The generated output is based on the content that actually exists on the page.
It does **not** invent values from unrelated assumptions, and it does **not** overwrite existing meta fields.

---

## Design principles

MetaMate AI follows a few simple rules:

- **Simple over advanced**
- **Clear UX over hidden automation**
- **No overwriting existing content**
- **Use the actual page text as source**

---

## Closed source, free to use

MetaMate AI is distributed as a compiled package.

- Free to use
- Source code is not publicly distributed
- No source-code repository is required for normal usage

---

## Support

Questions, issues, and feature requests can be handled through the project documentation repository or issue tracker.

---

## Links

- NuGet package: _add link after publishing_
- Documentation / support: _add GitHub docs repo link_
- Umbraco Marketplace: _add link after approval_

---

## Version

Current release: **1.0.0**
