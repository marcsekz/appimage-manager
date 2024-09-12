# Appimage repo
- json
- __see repo json for exact format__
- info:
  - name
  - type (github/other)
  - release list url [only for other type]
  - download url prefix [optional, only for other type]
  - repo name [only for github type]
  - pretty name
  - icon [only icon name]
  - version format (regex)
  - filename format (regex)

# Local DB
## Installed packages
Column name | Column type
------------|------------
name | TEXT UNIQUE NOT NULL
installed_version | TEXT NOT NULL
disable_autoupdate | INT [1 to disable]
repo_id | INT FK NOT NULL

## Repos
Column name | Column type
------------|------------
id | INT PK NOT NULL
name | TEXT NOT NULL
url | TEXT NOT NULL
local_version | TEXT