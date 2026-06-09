# Official Statistics Textbook — Posit Cloud Setup

## Files to Upload (all go into ONE project folder, no subfolders)

Upload ALL of these files directly into your Posit Cloud project:

| File | Purpose |
|------|---------|
| `index.Rmd` | Title page + Preface |
| `01-chapter1.Rmd` | Chapter 1 content |
| `02-chapter2.Rmd` | Chapter 2 content |
| `03-chapter3.Rmd` | Chapter 3 content |
| `04-chapter4.Rmd` | Chapter 4 content |
| `05-backmatter.Rmd` | Glossary + References |
| `_bookdown.yml` | Tells bookdown the file order |
| `_output.yml` | Output format settings |
| `style.css` | HTML styling |
| `references.bib` | Bibliography entries |

## How to Build the Book

### Step 1 — Install bookdown (first time only)
Open the Console in RStudio and run:
```r
install.packages("bookdown")
```

### Step 2 — Build the book
In the Console, run:
```r
bookdown::render_book("index.Rmd")
```

Or use the Build tab → Build Book button.

### To build only HTML (faster for preview):
```r
bookdown::render_book("index.Rmd", "bookdown::gitbook")
```

### To build only PDF:
```r
bookdown::render_book("index.Rmd", "bookdown::pdf_book")
```

## Adding Your Content

- Open any chapter file (e.g., `01-chapter1.Rmd`) and replace the `*[Add content here]*` lines with your actual text.
- Use `##` for section headings and `###` for sub-sections.
- Bold text: `**this is bold**`
- Numbered list: just type `1.`, `2.`, `3.`
- Bullet list: use `-` at the start of each line

## Adding a Table

```
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |
```

## Adding a Formula

Inline formula: `$CBR = \frac{B}{P} \times 1000$`

Display formula:
```
$$CBR = \frac{B}{P} \times 1000$$
```
