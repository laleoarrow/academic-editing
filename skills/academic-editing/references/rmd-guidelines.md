# R Markdown Best Practices for Academic Writing

## Reproducibility
- **Dynamically Generate Everything**: All figures, tables, and results should be computed within the document. Avoid hard-coding numbers or including external static images of results.
- **Set Seeds**: If using random processes (simulations, stochastic clustering), set a seed at the start of the chunk.

## Structure & Metadata
- **Informative YAML**: Include title, author, date, and abstract. Specify `bibliography` and `csl` for automated citation management.
- **Naming Chunks**: Always name code chunks (e.g., ````{r data-preprocessing}```) for better debugging and organized output.

## Code Chunk Management
- **Global Options**: Use `knitr::opts_chunk$set()` to define defaults (e.g., `echo=TRUE`, `warning=FALSE`, `message=FALSE`).
- **One Output Per Chunk**: Aim for one major figure or table per chunk to make cross-referencing easier.
- **Cache with Caution**: Use `cache=TRUE` for long-running computations but ensure dependencies are correctly tracked.

## Citations
- **BibTeX Integration**: Use `@citation_key` for in-text citations.
- **Reference Section**: End the document with a `# References` header.

## Visuals
- **Vector Graphics**: Prefer PDF or SVG for figures in print-ready manuscripts (e.g., `dev='pdf'`).
- **Captions**: Use `fig.cap` and `tab.cap` in chunk headers for automatic numbering.

## Formatting
- **Inline R**: Use `` `r function()` `` to insert variables directly into text.
- **rticles**: Utilize the `rticles` package for journal-specific LaTeX templates.
