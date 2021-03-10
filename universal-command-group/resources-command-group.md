---
title: resources Command group
order: 4
apiProperties:
  - property: -d, --dry
    description: Validate and view the result of an apply operation without persisting changes
  - property: --namespace strings
    description: List of namespaces that should be affected. Any resources outside of the listed namespaces will not be applied.
---

The resources command group provides built-in, cross-service commands that enable project-wide configuration to be managed as code.

## apply

**Usage**

```cli
yext resources apply [SOURCE-DIR] [flags]
```

**Flags**

-d, --dry
Validate and view the result of an apply operation without persisting changes
-f, --force
Force apply resources without a confirmation prompt
--namespace strings
List of namespaces that should be affected. Any resources outside of the listed namespaces will not be applied.
--on-missing-dependencies string
One of “ERROR”, “IGNORE”, or “ADD”. This determines the behavior of the apply if there are missing dependencies. The default value is “ERROR”. 

ERROR - will not complete the apply and output an error
IGNORE - will silently not complete the apply
ADD - will apply the files and add the missing dependencies
-h, --help
Help for resources apply


Applies configuration stored in the source directory to the account that the current configuration is pointing to. 
diff
Usage
yext resources diff [SOURCE-DIR] [flags]

Flags
-h, --help
Help for resources diff


Prerequisites
You must have Git installed in order to run this command. If Git is not installed, please follow the instructions on the Git website before running this command.

Behavior
Displays the differences between your local version of resources and your resources stored in Yext.
pull
Usage
yext resources pull [DESTINATION-DIR] [flags]

Flags
--include-system-dependencies
Pull the system dependencies of the account in addition to resources
--name strings
List of resource names. If this is included, only resources with the specified names are returned.
--namespace strings
List of namespaces. If this is included, only resources in the listed namespaces are returned.
--type strings
List of resource types. If this is included, only resources of the listed types will be returned. 
-h, --help
Help for resources pull


Pulls/fetches configuration from Yext and stores them in code files at the specified destination directory. Files are pulled from the Yext account specified by the current configuration.
