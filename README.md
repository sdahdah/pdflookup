# pdflu

Command line tool to find BibTeX for academic papers using Crossref and arXiv.

Prompt visual style inspired by Pacman.

## Sample config

```cfg
[pdflu]
# Number of pages to parse in a PDF
max_pages = 2
# If a parsed text box contains more than this many lines, it's not made part
# of the query because it's assumed to be part of the main body.
max_text_lines = 4
# If a parsed text box has this many words or less, it's not made part of the
# query.
min_text_words = 2
# If a parsed text box contains more than this many words, it's not made part
# of the query because it's assumed to be part of the main body.
max_text_words = 30
# Hard limit on the number of characters in a query.
max_query_chars = 200
# Number of results to fetch from each service (Crossref, arXiv).
max_query_results = 5
# Number of results to display in the prompt.
disp_query_results = 5
# Put an email here to gain access to the Crossref API's polite pool, which
# gives better performance. For more info, see
# https://github.com/CrossRef/rest-api-doc#good-manners--more-reliable-service
polite_pool_email = you@email.com
# If true, copies final result to clipboard
use_clipboard = false
# Number of lines of PDF to show (using `s` command in prompt)
show_first_lines = 10
```

## To do

- [x] Replace tabs with spaces
- [x] Add "show more" prompt
- [x] Open PDF
- [ ] Add override for `xdg-open`
- [ ] Clean up debug printing and logging
- [ ] Add manual query
- [ ] Add autoselect output
- [ ] Add library mode for bibmgr
- [ ] Add default config
- [ ] Add colour choices in config
- [ ] Add documentation in code
- [ ] PyPI
- [ ] Mac config location? https://stackoverflow.com/questions/3373948/equivalents-of-xdg-config-home-and-xdg-data-home-on-mac-os-x
