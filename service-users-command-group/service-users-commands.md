---
title: Service Users Commands
order: 1
apidoc: true
sidebarLinks:
- id: activate
  title: 'activate'
- id: create
  title: 'create'
- id: list
  title: 'list'
- id: remove
  title: 'remove'
---

Service users are non-human users that are authenticated to process Yext CLI commands on an account or project. Running Yext CLI commands using a service user will trigger promptless interaction, which enables programmatic and scripting use cases. 

The **service-users** command group allows you to create and manage these service users. There are four major commands in this command group:

* **create** - Used to create a service user with a specified name
* **activate** - Used to authenticate a service user based on a key file
* **list** - Outputs all the service users in the current session
* **remove** - Removes a service user from the current session


Each service user that is created will have a corresponding **key file** that is generated upon creation. This key file is the authentication for the service user to its associated account or project.

\
\

## Activate

Activates a service user given a key or key file, and changes the current session to that of the service user. Subsequent commands are executed under the newly activated service user.


### Usage
```cli
yext service-users activate [flags]
```

### Flags

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

\
\

## Create

Creates a service user with the specified name. The created service user details are encrypted and written to the provided key-file-path. 


### Usage
```cli
yext service-users create [NAME] [KEY-FILE-PATH] [flags]
```

### Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for service-users create |
\
\
{{< /classic-table >}}


\
\

## List

Lists all the service users under the current session. The currently selected service user is saved to the given path. 


### Usage
```cli
yext service-users list [PATH] [flags]
```

### Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for service-users list |
| `--download-any-user`    | Downloads any existing service user to the specified path. Useful for scripting use cases. |
\
\
{{< /classic-table >}}

\
\

## Remove

Removes the service user with the provided name. 


### Usage
```cli
yext service-users remove [NAME] [flags]
```

### Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for service-users create |
\
\
{{< /classic-table >}}



