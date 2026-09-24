# rlee822.github.io
# Personal Website

This repository contains my Quarto personal website, including computational posts written in R and Python.

## Requirements

This site was built using:

- Quarto: 1.10.18
- uv: uv 0.12.5 (210d1f678 2026-08-14 aarch64-apple-darwin)
- R: R version 4.6.1 (2026-06-24) -- "Happy Hop"

## Build instructions

Clone the repository:

```bash
git clone https://github.com/rlee822/rlee822.github.io.git
cd rlee822.github.io
```

### Install the Python environment

From the top level of the repository, run:

```bash
uv sync
```
### Restore the R environment

From the top level of the repository, start R:

```bash
R
```

Then run:

```r
renv::restore(project = getwd())
```

Exit R:

```r
q()
```
### Render the website

From the top level of the repository, run:

```bash
uv run quarto render
```
### Built site

The rendered website is created in the `docs/` directory.

To preview the website locally, run:

```bash
uv run quarto preview
```
### Data

The Python post uses the Palmer Penguins dataset from the `palmerpenguins` package.

Data source: [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/), Palmer Station Antarctica LTER.

The dataset is provided by the installed package, so the build does not need to download the data from an external URL at render time.


