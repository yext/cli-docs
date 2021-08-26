---
title: view records
order: 4

---

Displays the most recent input or output records of a stream. Will only display a maximum of 10 records.

## Usage
```cli
yext streams view records <streamId> [flags]
```

## Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-c`, `--color`    | Colorize the output. (default true) |
| `-d`, `--display strings`    | Parts of the record to display. Allowed values: key, body, headers. (default [key,body]) |
| `-f`, `--follow`    | maintain connection and receive new records until cancelled |
| `-h`, `--help`    | Help for resources diff |
| `-l`, `--limit int`    | Number of records to display. 10 is the maximum number of records which will be displayed. |
| `-t`, `--type string`    | Whether records displayed should be the “input” records (before any projections or transformations) or the “output” records which are produced by the Stream. Allowed values: input, output. (default "output") |
\
\
{{< /classic-table >}}


