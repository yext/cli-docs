---
title: Resources Commands
order: 1
apidoc: true
sidebarLinks:
- id: apply
  title: 'apply'
- id: diff
  title: 'diff'
- id: pull
  title: 'pull'
- id: copy
  title: 'copy'
apiProperties:
  - property: -d, --dry
    description: Validate and view the result of an apply operation without persisting changes
  - property: --namespace strings
    description: List of namespaces that should be affected. Any resources outside of the listed namespaces will not be applied.
---

The **resources** command group will allow you to manage Configuration as Code (CaC) resources in your Yext accounts. Much of the configuration and setup of your Yext account is actually stored in JSON configuration files that can be modified programmatically through the CLI or Admin Console. This provides you, as developers, a high level of flexibility to manage your account's resources in whatever way makes the most sense with your existing applications. 


There are three major commands in this command group:

* **pull**  - Save Configuration as Code resources from a Yext account to your local machine in a directory structure

* **apply** - Configure a Yext account with Configuration as Code resources stored on your local machine

* **diff** - Show the diff between the resources in a Yext account and your local version


\
\

How do these commands all fit together? If you think about this in the context of a workflow, you would want to: 

1. Run `yext init` to initialize your account
2. Run `yext resources pull [DESTINATION-DIR]` to pull your account's configuration files locally. 
4. Make modifications to files or add new files on your machine
5. Run `yext resources diff [SOURCE-DIR]` (optionally) to review your changes
6. Run `yext resources apply [SOURCE-DIR]` to update your account

You can follow along in our [Getting Started with Updating CaC Resources via CLI guide](/guides/getting-started-cli-resources). 

\
\

### Common Use Cases

You can combine these commands to do things like:

* Copy configuration from your Sandbox account to your Production account
* Populate a Sandbox testing account with production configuration 
* Save your Yext account’s configuration to revert to later on


{{< protip-large title="Want to learn more about CaC?" color="#E6EDDD" icon="reading" >}}
You can learn more about Configuration as Code in this [training module](https://hitchhikers.yext.com/tracks/solution-templates/sol201-configuration-as-code/) and you can explore available resource types in the [CaC reference documentation](https://developer.yext.com/cac/conversion-action/). 
{{< /protip-large >}}

\
\

## apply

Applies configuration stored in the source directory to the account that the current credential is pointing to. 

### Usage
```cli
yext resources apply [SOURCE-DIR] [flags]
```

### Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for resources apply |
| `-d`, `--dry` | Validate and view the result of an apply operation without persisting changes |
| `-f`, `--force` | Force apply resources without a confirmation prompt |
| `--namespace strings` | List of namespaces that should be affected. Any resources outside of the listed namespaces will not be applied. See examples below. |

\
\
{{< /classic-table >}}

**Example usage of `--name` flag**

If you are trying to: 

  * Apply resources in **myFolder** that are in the default namespace, run: 
    ```cli
    yext resources apply myFolder --namespace default
    ```

  * Apply resources in **myFolder** that are in the default namespace OR **myNamespace**

    ```cli
    yext resources apply myFolder --namespace default,myNamespace
    ```

\
\

## diff

Displays the differences between your local version of resources and your resources stored in Yext. This is powerful for operations where you want to review the changes before they are applied. 


### Usage
```cli
yext resources diff [SOURCE-DIR] [flags]
```

### Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for resources diff |
\
\
{{< /classic-table >}}



### Prerequisites

You must have Git installed in order to run this command. If Git is not installed, please follow the instructions (on the Git website)[https://git-scm.com/book/en/v2/Getting-Started-Installing-Git] before running this command.

\
\


## pull

Pulls/fetches configuration from Yext and stores them in code files at the specified destination directory. Files are pulled from the Yext account specified by the current credential.

### Usage
```cli
yext resources pull [DESTINATION-DIR] [flags]
```

### Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for resources pull |
| `--name strings` | List of resource names. If this is included, only resources with the specified names are returned. Resources are specified with their full id including namespace. See examples below. |
| `--namespace strings` | List of namespaces. If this is included, only resources in the listed namespaces are returned. See examples below. |
| `--type strings` | List of resource types. If this is included, only resources of the listed types will be returned. A resource type is specified by the path after https://schema.yext.com/config/ in the $schema field of its Config as Code JSON schema definition. JSON schema definitions can be found [here](https://developer.yext.com/cac/conversion-action/). |
| `--exclude strings` | List of resource types to exclude. If this is included, the resources of the listed types will be excluded. A resource type is specified by the path after https://schema.yext.com/config/ in the $schema field of its Config as Code JSON schema definition. JSON schema definitions can be found [here](https://developer.yext.com/cac/conversion-action/). |
| `--organize-by-resource-type` | Organize the pulled resources by resource type, as opposed to organize by namespace. See examples below. |
\
\
{{< /classic-table >}}


**Example usage of `--name` flag**

If you are trying to: 

  * Pull resource called myResource in the default namespace **to myFolder**, run:
    ```cli
    yext resources pull myFolder --name myResource
    ```

  * Pull resource called myResource in the namespace myNamespace **to myFolder**, run: 
    ```cli
    yext resources pull myFolder --name myNamespace_myResource
    ```

  * Pull resources called myResource1 and myResource2 in the default namespace **to myFolder**, run: 
    ```cli
    yext resources pull myFolder --name myResource1,myResource2
    ```

\
\

\

\


**Example usage of `--namespace` flag**

If you are trying to: 

  * Pull resources in the default namespace to **myFolder**, run: 

    ```cli
    yext resources pull myFolder --namespace default
    ```

  * Pull resources in the default namespace and myNamespace to **myFolder**, run: 
    ```cli
    yext resources pull myFolder --namespace default,myNamespace
    ```


\
\

\

\


**Example usage of `--type` Flag**

  * Pull all entity-type resources to **myFolder**, run: 
    ```cli
    yext resources pull myFolder --type km/entity-type 
    ```

  * Pull all entity-type resources and all role resources to **myFolder**, run: 
    ```cli
    yext resources pull myFolder --type km/entity-type,platform/role
    ```

**Example usage of `--exclude` Flag**

  * Pull all resources except km/entity to **myFolder**, run: 
    ```cli
    yext resources pull myFolder --exclude km/entity 
    ```

  * Pull all resources except entity-type and role resources to **myFolder**, run: 
    ```cli
    yext resources pull myFolder --exclude km/entity-type,platform/role
    ```


\
\

\

\


**Example usage of `--organize-by-resource-type` Flag**

  * Pull resources and organize by resource type, run:
    ```cli
    yext resources pull myFolder --organize-by-resource-type 
    ```


\
\

## copy

Applies configurations stored in the source account to the destination account.

Notable operations the copy command does:

1. Pulls dependencies.json from source account and applies to the destination account (if destination account is a non-production account).
2. Pulls with pages-force-template true and then edits the pages/site-config JSONs by copying value at JSON path /repoConfig/templateRepo to /repoConfig/targetRepoName
3. Edits the km/entity config JSONs by removing JSON paths /content/googleAttributes and /content/categoryIds

### Usage
```cli
yext resources copy [flags]
```

### Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for resources copy |
\
\
{{< /classic-table >}}


