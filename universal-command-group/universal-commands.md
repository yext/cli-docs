---
title: Universal Commands
order: 1
apidoc: true
sidebarLinks:
- id: init
  title: 'init'
- id: info
  title: 'info'
- id: completion
  title: 'completion'
---

## init

This command will take you through a flow to select existing or create a new credential. This includes specifying a universe (production, sandbox) using the --universe flag, selecting or creating new credentials, and choosing a Yext account to work with.

### Usage
```cli
yext init [ACCOUNT-ID] [flags]
```

### Flags 

{{< classic-table >}}
| Flag     | Description   |
| --------------- |:-------------:|
| `-h`, `--help`      | Help for init |
| `-u`, `--universe`  | The global environment this credential is for, either “production” or “sandbox”. By default this value is “production”. |
\
\
{{< /classic-table >}}


\
\


## info

Shows the current credential settings, including credential name, universe, account ID and account name. Writes the output to path if a path is provided. 

### Usage
```cli
yext info [path] [flags]
```

### Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for info |
\
\
{{< /classic-table >}}


\
\


## completion

Sets up autocomplete for all subsequent sessions.

### Usage
```cli
yext completion [bash | zsh | powershell ]
```

### Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for completion |
\
\
{{< /classic-table >}}



### Prerequisites
You must have shell completion enabled in your command line environment. If you don’t have shell completion enabled, you can enable it by following one of the following steps:

**For bash:**

* Add `[ -f /usr/local/etc/bash_completion ] && . /usr/local/etc/bash_completion` to your bash profile.

**For zsh:**

* Run `echo "autoload -U compinit; compinit" >> ~/.zshrc`

**For powershell**

* Run `yext completion powershell >> $profile`
\
\

\

\

### Setting up Autocomplete
If you are using bash on Linux, run
```cli
yext completion bash > /etc/bash_completion.d/yext
```

If you are using bash on Mac OSX, run
```cli
yext completion bash > /usr/local/etc/bash_completion.d/yext
```

If you are using zsh, run
```cli
yext completion zsh > “${fpath[1]}/_yext”
```

If you are using Powershell on Windows, run:
```cli
yext completion powershell | Out-String | Invoke-Expression
```

After running the appropriate command for your system, you must start a new shell session to begin using autocomplete.