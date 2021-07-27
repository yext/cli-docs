---
title: refresh list
order: 2
---

List all refresh jobs. By default, the 10 most recent refresh jobs will be displayed. 

## Usage
```cli
yext streams refresh list [flags]
```

## Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for resources apply |
| `-n`, `--number` | Number of refresh jobs to display. Defaults to 10. |
| `-s`, `--stream` | The ID of the specific stream for which you want refresh jobs listed.  |
| `-d`, `--destination` | Filter to only streams for a specific destination. Allowed values: streamsapi, answers, pages, listings |
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


