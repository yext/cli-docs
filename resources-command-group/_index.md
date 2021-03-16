---
title: Resources Command Group
order: 5
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