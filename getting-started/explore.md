---
title: Exploring Commands & Using the Help Flag
order: 2

---


Now that you’re set up with the Yext CLI, find out what you can do by running the command: 

```cli
yext
```

This will output a quick how-to guide and a list of available commands in the CLI. You should get a response like this:
 
```cli
$ yext

This is a beta version of the Yext Command Line Interface

yext is a command line interface to configure Yext services

The first parameter is the name of the top-level command group (or, in a few special cases, top-level commands)
Each command group itself consists of commands, additional command groups, or both.
These are specified left to right until a command is reached.
Following the command are positional arguments. The meaningful positional arguments depend only on the command.
Finally, flag arguments are specified, which can include both command-specific flags (like --comprehensive) or flags that have a global meaning (such as --project). These can be either booleans or have values.

For Example:
yext init
 - initializes the yext configuration

Usage:
  yext [command]

Available Commands:
  completion    Generate completion script
  help          Help about any command
  info          Print current configuration context
  init          Create or modify configurations
  resources     Manage project-wide configuration as code
  service-users Manage prompt-less interaction with the Yext CLI
  version       Display CLI version

Flags:
  -h, --help   help for yext

Use "yext [command] --help" for more information about a command.
```

\
\

## Getting Help 

If you want to learn more about a command, simply run the command with the help flag (--help, or -h) to get more information about that command group and its fundamental operations. 

Let’s try it with `yext resources`:

```cli
yext resources --help
```

You should see a response like this: 

```cli
This is a beta version of the Yext Command Line Interface

The resources command group provides built-in, cross-service commands that enable project-wide configuration to be managed as code.

The fundamental operations are:

pull - pulling/fetching configuration from the services in a resource-oriented model and storing them in code files

apply - making the configuration on the server match the state defined in source files. (This includes diff with the use of dry-run).

Usage:
  yext resources [command]

Available Commands:
  apply       Apply configurations from source directory
  diff        Diff local resources against resources in Yext
  pull        Pull configurations to destination directory

Flags:
  -h, --help   help for resources

Use "yext resources [command] --help" for more information about a command.
```

The resulting help text tells us that `resources` is a **command group**, lists the available commands in the group, and describes how to get further help on any command within the group. 

Using the help flag is a great way to learn about the Yext CLI and view documentation in-line. You can also always come back to this Yext CLI reference page for more detailed documentation.

If you run into an error while running a command in the Yext CLI, a good place to start is checking out the help text for that command. You might be missing a required option, and the help text will provide that information. If you're still stuck, we recommend posting in our (Community)[https://hitchhikers.yext.com/community/c/yext-cli/37]. 
