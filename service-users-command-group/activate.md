---
title: activate
order: 1

---

Activates a service user given a key or key file, and changes the current session to that of the service user. Subsequent commands are executed under the newly activated service user.


## Usage
```cli
yext service-users activate [flags]
```

## Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for service-users activate |
| `--key string`    | Key to activate a service user (the value contained in the key file) |
| `--key-file string`    | Path to the key file to activate a service user |
| `-u`, `--universe string`    | The global environment this configuration is for, either “production” or “sandbox”. By default this value is “production" |

\
\
{{< /classic-table >}}

