# Fork information

This is a fork of xuhcc's project, to experiment with MkDocs, text
wrapping, etc.

The MkDocs prototype is at https://bradyt.github.io/beancount-docs/.

# Beancount Documentation

https://xuhcc.github.io/beancount-docs/

Source files are in [docs](docs/) directory.

These documents in markdown format are automatically generated from [official Beancount Documentation](http://furius.ca/beancount/doc/index).

## Beancount Google Doc converter

### Installation

Install dependencies (python 3 is required, virtualenv is recommended):

```
pip install -r requirements.txt
```

### Usage

Export and convert single document:

```
python export.py document "100tGcA4blh6KSXPRGCZpUlyxaRUwFHEvnz_k9DyZFn4" doubleentry.docx
python export.py drawings "100tGcA4blh6KSXPRGCZpUlyxaRUwFHEvnz_k9DyZFn4" drawings
python export.py convert doubleentry.docx doubleentry.md --drawing-dir=drawings
```

Export and convert all documents:

```
python crawl.py
```

## Website

Generate static website from markdown documents:

```
bundle install --path vendor/bundle
bundle exec jekyll serve --source docs/
```
