---
title: refresh list
order: 2
---

Lists refresh jobs filtered by the given flags. By default, the 10 most recent refresh jobs will be displayed.

## Usage
```cli
yext streams refresh list [flags]
```

## Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-d`, `--destination` (string) | Filter to only streams for a specific destination. Allowed values: streamsapi, answers, pages, listings |
| `-h`, `--help`    | Help for resources apply |
| `-l`, `--limit` | Number of refresh jobs to display. (default 10) |
| `-p`, `--pageToken` (string) | If a response to a previous request contained the nextPageToken field, pass that field's value as the pageToken parameter to retrieve the next page of data. |
| `-s`, `--stream` | The ID of the specific stream for which you want refresh jobs listed.  |
\
\
{{< /classic-table >}}

This command will return a table with information about the refresh job:

* Refresh Job ID
* Stream ID
* Stream Destination
* Start Time
* Status
* Output Records Produced
* Errors


