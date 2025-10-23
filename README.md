# JDC Quarto Template

A unified Quarto template for creating JDC-branded presentations and reports with consistent styling and branding.

## Overview

This template provides a single, consolidated setup for creating multiple output types:
- **Presentations** (RevealJS slides)
- **HTML Reports** (interactive web documents)
- **PDF Reports** (print-ready documents)

All outputs share the same JDC brand configuration, ensuring consistent colors, fonts, and logos across all documents.

## Template Structure

```
jdc-template/
├── _brand.yml           # JDC brand configuration (colors, fonts, logos)
├── _quarto.yml          # Project-wide Quarto configuration
├── _extensions/         # Custom JDC formats (jdc-revealjs, jdc-html)
│   └── jdc/
├── slides.qmd           # Template for RevealJS presentations
├── report-html.qmd      # Template for HTML reports
├── report-pdf.qmd       # Template for PDF reports
└── README.md            # This file
```

## Quick Start

### 1. Prerequisites

- [Quarto](https://quarto.org/docs/get-started/) (version 1.5.0 or higher)
- For PDF output: A LaTeX distribution (e.g., TinyTeX, TeX Live, or MiKTeX)

### 2. Rendering Documents

Each `.qmd` file can be rendered independently:

```bash
# Render presentation slides
quarto render slides.qmd

# Render HTML report
quarto render report-html.qmd

# Render PDF report
quarto render report-pdf.qmd
```

Or render all documents at once:

```bash
quarto render
```

### 3. Preview in Browser

For live preview while editing:

```bash
quarto preview slides.qmd
quarto preview report-html.qmd
```

## Available Templates

### Slides (RevealJS)

**File:** `slides.qmd`
**Format:** `jdc-revealjs`
**Output:** HTML presentation

Features:
- JDC-branded title slide with logo
- Custom slide layouts and color schemes
- Incremental reveals
- Speaker notes
- Two-column layouts
- Custom CSS classes for styling

### HTML Report

**File:** `report-html.qmd`
**Format:** `jdc-html`
**Output:** Interactive HTML document

Features:
- JDC branding and styling
- Automatic table of contents
- Code folding and syntax highlighting
- Callout boxes (note, tip, warning, important)
- Brand color helper classes
- Responsive two-column layouts

### PDF Report

**File:** `report-pdf.qmd`
**Format:** `pdf`
**Output:** PDF document

Features:
- Professional PDF layout
- Automatic table of contents
- Section numbering
- Mathematical equation support (LaTeX)
- Callout boxes
- Print-optimized formatting

## Customization

### Modifying Brand Settings

Edit `_brand.yml` to customize:
- Brand colors (primary, secondary, etc.)
- Typography (fonts, weights)
- Logos

### Project-Wide Settings

Edit `_quarto.yml` to adjust:
- Default format options
- Code execution settings
- Resource embedding

### Document-Specific Settings

Each `.qmd` file has a YAML header where you can customize:
- Title, subtitle, author, date
- Format-specific options
- Whether to embed resources

Example:

```yaml
---
title: My Custom Title
subtitle: A Subtitle
author: John Doe
date: 2025-10-23
format: jdc-html
embed-resources: true
---
```

## Tips and Best Practices

1. **Choose the Right Template:**
   - Use `slides.qmd` for presentations
   - Use `report-html.qmd` for interactive web reports with code
   - Use `report-pdf.qmd` for print-ready documents

2. **Embed Resources:**
   - Set `embed-resources: true` to create standalone files
   - Useful for sharing documents without external dependencies

3. **Brand Consistency:**
   - All templates automatically use JDC brand colors and fonts
   - Use brand helper classes (`.text-blue`, `.bg-blue`, etc.) for consistency

4. **Code Integration:**
   - All templates support executable code chunks (Python, R, Julia, etc.)
   - Use code chunks to generate dynamic content

## Additional Resources

- [Quarto Documentation](https://quarto.org/docs/)
- [Quarto Presentations](https://quarto.org/docs/presentations/)
- [Quarto HTML Documents](https://quarto.org/docs/output-formats/html-basics.html)
- [Quarto PDF Documents](https://quarto.org/docs/output-formats/pdf-basics.html)

