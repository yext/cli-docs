---
title: apply
order: 1
apiProperties:
  - property: -d, --dry
    description: Validate and view the result of an apply operation without persisting changes
  - property: --namespace strings
    description: List of namespaces that should be affected. Any resources outside of the listed namespaces will not be applied.

---

Applies configuration stored in the source directory to the account that the current credential is pointing to. 

## Usage
```cli
yext resources apply [SOURCE-DIR] [flags]
```

## Flags

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

