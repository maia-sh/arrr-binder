# Instructions to create Binder

1. Create local repository with:
  - R Project
  - .R files for analysis
  - README.md
  *Note: Do not create DESCRIPTION.txt or Dockerfile.txt. Holepunch creates this.*

2. Load holepunch package
`library(holepunch)`

3. Write compendium description, with dependencies
```{r}
write_compendium_description(package = "Your compendium name", 
                             description = "Your compendium description")
```
4. When prompted, edit DESCRIPTION.txt

4. Write dockerfile
```{r}
write_dockerfile(maintainer = "your_name")
```
*Note: Holepunch will automatically pick the date of the last modified file, match it to that version of R and add it here. You can override this by passing r_date to some arbitrary date for which a R version exists.*

5. Generate badge text and automatically copy to clipboard
```{r}
generate_badge()
```

6. Paste badge text into README.md

7. Commit and push code to GitHub **public** repository

8. Build binder by either:
  - Script in RStudio: `build_binder()`
  - Click badge in README.md (either on GitHub or RStudio README.md Preview)

<!-- badges: start -->
[![Launch Rstudio Binder](http://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/maia-sh/arrr-binder/master?urlpath=rstudio)
<!-- badges: end -->

