---
title: Resources Commands
order: 4
apidoc: true
sidebarLinks:
- id: copy
  title: 'copy'
---

Applies configurations stored in the source account to the destination account.

Notable operations the copy command does:

1. Pulls dependencies.json from source account and applies to the destination account (if destination account is a non-production account).
2. Pulls with pages-force-template true and then edits the pages/site-config JSONs by copying value at JSON path /repoConfig/templateRepo to /repoConfig/targetRepoName
3. Edits the km/entity config JSONs by removing JSON paths /content/googleAttributes and /content/categoryIds

## Usage
```cli
yext resources copy [flags]
```

## Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for resources copy |
\
\
{{< /classic-table >}}

