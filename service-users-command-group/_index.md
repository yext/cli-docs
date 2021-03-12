---
title: Service Users Command Group
order: 5
---

Service users are non-human users that are authenticated to process Yext CLI commands on an account or project. Running Yext CLI commands using a service user will trigger promptless interaction, which enables programmatic and scripting use cases. 

The **service-users** command group allows you to create and manage these service users. There are four major commands in this command group:

* **create** - Used to create a service user with a specified name
* **activate** - Used to authenticate a service user based on a key file
* **list** - Outputs all the service users in the current session
* **remove** - Removes a service user from the current session


Each service user that is created will have a corresponding **key file** that is generated upon creation. This key file is the authentication for the service user to its associated account or project.