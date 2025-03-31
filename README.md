# Quarto Microbiome Reports

A collection of Quarto templates and formats for creating publication-ready microbiome analysis reports.

## 📊 Features

- Multiple output formats:
  - Interactive dashboards
  - HTML reports
  - PDF documents
  - Scrollytelling presentations (Just and idea, we need to check)
- Custom fonts and styling
- Built-in bibliographic support
- Microbiome-specific templates

## 🗂️ Project Structure

```
quarto-templates/
├── assets/
├── config/
├── formats/
│   ├── pdf/
│   │   ├── _extensions/           # PDF-specific extensions
│   │   ├── _template.tex
│   │   ├── custom.scss
│   │   └── format-config.yml
│   ├── html/
│   │   ├── _extensions/           # HTML-specific extensions
│   │   ├── custom.scss
│   │   └── format-config.yml
│   └── [other-formats]/
├── templates/
│   ├── exploratory/
│   │   ├── exploratory.qmd
│   │   └── _includes/             # Content components specific to exploratory analysis
│   ├── stats/
│   │   ├── stats.qmd
│   │   └── _includes/
│   └── [other-report-types]/
└── _extensions/                   # Shared extensions used across multiple formats
    ├── custom-theme/
    ├── special-blocks/
    └── [other-shared-extensions]/
├── references.bib
├── parameters/   ## Check if is beter to pass parameters as separate files
```

## 🚀 Getting Started

1. Install [Quarto](https://quarto.org/docs/get-started/)
2. Clone this repository
3. Open the project in RStudio or VS Code
4. Start to create custom visualization in configuration files (scss, yml, tex etc)


## 📋 Prerequisites

- Quarto >= 1.3
- R >= 4.0
- Required R packages listed in the `.qmd` files

## 🎨 Customization

- Modify `_quarto.yml` for global settings
- Edit `_brand.yml` for styling preferences
- Custom fonts are available in the `fonts/` directory


## 📚 Citation

To make citations/references in templates, use bib files. You can add your own references in the `references.bib` file.
To cite in quarto, use the following:

1. Include in yml
```yaml
bibliography: references.bib
```
2. Cite in text

```
We use dada2 for analysis [@Callahan2016-fe]
```
3. Add a bibliography section in your document

```
## References

::: {#refs}
:::
```

4. Render the document to see the citations and bibliography
