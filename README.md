# rachelyan419.github.io


Personal website and blog of Rachel Yan, built with Quarto and published
with GitHub Pages at <https://rachelyan419.github.io>.
It includes two computational posts, one written in Python and one in R.

## Requirements

Install these first (versions used to build this site):

- [Quarto](https://quarto.org/docs/get-started/) 1.10.18
- [uv](https://docs.astral.sh/uv/) 0.12.6
- [R](https://cran.r-project.org/) 4.6.1 (`renv` installs itself on first use)

## Build the site

1. In a terminal, clone the repository and move into it:

```bash
   git clone https://github.com/rachelyan419/rachelyan419.github.io.git
   cd rachelyan419.github.io
```

2. In the same terminal, create the Python environment from `uv.lock`:

```bash
   uv sync
```

3. Still in the top-level folder of the repository, start R by typing `R`.
   Restore the R packages from `renv.lock`, then quit R:

```r
   renv::restore()
   q()
```

4. Back in the terminal, from the top-level folder, render the site:

```bash
   uv run quarto render
```

## Output

The built site is written to `docs/`.
Open `docs/index.html` in a browser, or run `uv run quarto preview`
to view it locally.

## Data

- **Python post:** the [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/)
  dataset (CC0), installed with the `palmerpenguins` Python package.
- **R post:** the [gapminder](https://cran.r-project.org/package=gapminder)
  dataset, installed with the `gapminder` R package
  (data from the Gapminder Foundation, CC BY 4.0).

No data files are committed to this repository. Both datasets are installed
with their packages, so rendering does not need network access beyond
installing the packages.