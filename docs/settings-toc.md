# Table of Contents Settings

Various settings are available for the table of contents widget, which provides a ToC navigation pane that allows navigation of a notebook based on markdown headings.

Section numbering style and the depth of the displayed headings are customisable.

The following settings are recommended to be set in `.jupyter/lab/user-settings/@jupyterlab/toc-extension/registry.jupyterlab-settings`:

```json
{
    "maximalDepth": 4,
    "numberingH1": true,
    "numberHeaders": false,
    "baseNumbering": 1
}
```