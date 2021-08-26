---
title: refresh status
order: 3

---

Print the status of a refresh job.

It is valid not to specify a refresh-job-id and only supply a streamId using the -s flag; in this case, the command will print the status of the most recent refresh job for the specified stream. 

## Usage
```cli
yext streams refresh status [<refresh-job-id>] [flags]
```

## Arguments

{{< classic-table >}}
| Argument     | Description   |
| ------------- |:-------------:|
| `refresh-job-id`    | The id of the refresh job. You can find this by running `yext streams refresh list` to view existing refreshes in your account.  |
\
\
{{< /classic-table >}}



## Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for resources pull |
| `-s`, `--stream` (string)   | The id of the stream. You can find this by running the `streams list` command. |
\
\
{{< /classic-table >}}


