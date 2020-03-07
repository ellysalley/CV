## Forked from https://github.com/nstrayer/cv

This repo contains the source-code and results of my CV built with the [pagedown package](https://pagedown.rbind.io) and [`googlesheets4` package.](https://googlesheets4.tidyverse.org/index.html)

## Structure

The main files are:

- `index.Rmd`: Source template for the cv, contains a variable `PDF_EXPORT` in the header that changes styles for pdf vs html. 
  - `index.html`: The final output of the template when the header variable `PDF_EXPORT` is set to `FALSE`.
  - `ellyhan_cv.pdf`: The final exported pdf as rendered by Chrome on my mac laptop. Links are put in footer and notes about online version are added. 
- `resume.Rmd`: Source template for single page resume. 
  - `resume.html`: Result for single page resume.
- `parsing_functions.R`: A series of small functions for parsing a position entry into the proper HTML format. Includes logic for removing links if needed etc..
- `gather_data.R`: Loads the data that makes up the body of both the CV and resume. Either pulls from a specified google sheet with info or multiple csvs. (Examples of both are provided in repo.)
- `csvs/*.csv`: A series of CSVs containing the information CV and resume. Included as examples if the non-googlesheets method of storing data is prefered.  
- `css/`: Directory containing the custom CSS files used to tweak the default 'resume' format from pagedown. 