# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Contents

This is a Python learning/study repository containing:

- **Jupyter notebooks** — Educational data analysis exercises from IBM Cognitive Class / Coursera (Data Analysis with Python course)
- **`marketplace-spec.md`** — Functional specification for a two-sided musical instruments marketplace

## Working with Notebooks

Run notebooks interactively with Jupyter:

```bash
jupyter notebook
```

Or run a specific notebook non-interactively:

```bash
jupyter nbconvert --to notebook --execute data-wrangling.ipynb
jupyter nbconvert --to notebook --execute review-introduction.ipynb
```

## Notebook Overview

- **`review-introduction.ipynb`** — Covers data acquisition with `pandas.read_csv()`, adding column headers, basic inspection (`head`, `tail`, `dtypes`, `describe`, `info`). Uses the UCI Automobile dataset loaded from a remote URL.
- **`data-wrangling.ipynb`** — Continuation of the data analysis course, covering data cleaning and transformation.

Both notebooks use the same Automobile dataset (205 rows, 26 columns) from IBM Cloud Object Storage. Missing values in this dataset are represented as `"?"` strings rather than `NaN`.

## Marketplace Specification

`marketplace-spec.md` defines a two-sided marketplace for buying and selling musical instruments. Key data models: `User` (with `buyer`/`seller`/`admin` roles), `SellerProfile`, `Listing`, `ListingImage`, `Order`, `OrderItem`. Order statuses flow: `Pending Payment` → `Paid` → `Processing` → `Shipped` → `Delivered` (with `Cancelled`/`Returned` as terminal states).
