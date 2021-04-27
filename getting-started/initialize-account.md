---
title: Link Your Account
order: 1

---

First, you’ll want to set up a connection to your Yext account and create a credential.  A **credential** is a profile that defines the context - environment and account that you are working in. If you work with multiple Yext accounts, you'll be able to easily switch between your credentials without having to provide your account ID. 

To get started, you’ll need to **Initialize your Account** by running the following command:

```cli
yext init
```

{{< protip-large color="#FFF8E5" >}}
If you would like to use the **sandbox environment** (e.g., for a playground account), you'll want to set your "universe" to sandbox using the `u` flag. Ex: 

```cli
yext init -u sandbox
```
{{< /protip-large >}}

Unless you already have a credential set up, when prompted select **Create new credentials**. 

```cli
? Please select one of the following options Create new credentials
```

Next, you'll need to input your account ID. You can find your Yext Account ID by looking in Account Settings > Personal Settings in the Account Information table or by pulling the ID out of the URL of your account after the /s/.  

For example: 

```cli
? Enter account ID (If you do not have a Yext account, please sign up at https://www.yext.com/signup and get the acconut ID from the URL '/s/<account ID>/...')
> 12345
```

This will take you to the browser. Finish up by authenticating into your account and returning to the terminal when done.

**Congrats, Now you're ready to start using the CLI!**

