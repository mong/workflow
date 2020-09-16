# Docker

## docker-compose qmongr

1. Find a database dump file `imongr_db_dump.sql.gz` and put it in the root folder `qmongr/`
2. Fire up docker-compose (`docker-compose up`)
3. Enter *RStudio* on http://localhost:8787/
4. *TBA*

## docker-compose imongr

1. Find a database dump file `imongr_db_dump.sql.gz` and put it in the folder `inst/`
2. Fire up docker-compose (`docker-compose up`)
3. Enter *RStudio* on http://localhost:8787/
4. Set up `imongr` inside docker. Either do `git clone git@github.com:mong/imongr` and create new project based on folder, or create new project based on git repository. Dependencies can be installed by first install `remotes` and then install `imongr` from `github`: `remotes::install_github("mong/imongr")`.
5. Define user, groups etc.
```
Sys.setenv(SHINYPROXY_USERNAME="<my-user-name>")
Sys.setenv(SHINYPROXY_USERGROUPS="MANAGER") # or PROVIDER (not sure how to add both at the same time...)
```
