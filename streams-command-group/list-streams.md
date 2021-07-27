---
title: list-streams
order: 1
---

To simplify the user experience of using the CLI to monitor streams, we have a list-streams command which lists all the streams in an account. By default, the 10 most recently updated streams will be displayed. 

Note: The stream-config resource is read-only, which means stream-config resources will not be visible by default in Admin Console (though they will be included in CLI pulls). In order to view a read-only resource, a user will need to check a flag in the Admin Console settings, or use this command in the CLI. 



## Usage
```cli
yext streams list-streams [flags]
```

## Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for resources apply |
| `-n`, `--number` | Number of streams to display. Defaults to 10. |
| `-d`, `--destination` | Filter to only streams for a specific destination. Allowed values: streamsapi, answers, pages, listings |
\
\
{{< /classic-table >}}


This command will return a table with the following information about each stream:

* Stream ID
* Source
* Filter
* Destination
* Last Update Time 
* Output Record Count (Current)

