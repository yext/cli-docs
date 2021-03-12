---
title: pull
order: 3

---

Pulls/fetches configuration from Yext and stores them in code files at the specified destination directory. Files are pulled from the Yext account specified by the current credential.

## Usage
```cli
yext resources pull [DESTINATION-DIR] [flags]
```

## Flags

{{< classic-table >}}
| Flag     | Description   |
| ------------- |:-------------:|
| `-h`, `--help`    | Help for resources pull |
| `--name strings` | List of resource names. If this is included, only resources with the specified names are returned. Resources are specified with their full id including namespace. See examples below. |
| `--namespace strings` | List of namespaces. If this is included, only resources in the listed namespaces are returned. See examples below. |
| `--type strings` | List of resource types. If this is included, only resources of the listed types will be returned. A resource type is specified by the path after https://schema.yext.com/config/ in the $schema field of its Config as Code JSON schema definition. JSON schema definitions can be found [here](https://developer.yext.com/cac/conversion-action/). |
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

