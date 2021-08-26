---
title: Streams CLI Command Group
order: 6
---

## Command Group Overview

The Streams CLI commands are intended to provide visibility into the Streams powering your downstream experiences. When using the Streams CLI commands, you will be interacting directly with the Streams which have been configured to power the various Yext products you are using. For example, you could obtain visibility into a Stream powering a specific Streams Endpoint, Pages Template, or Answers vertical. 

## How to use the Streams Commands

Let’s walk through how you might leverage the Streams CLI.

Since Streams are derived from your downstream experiences, rather than defined by the user, you may not be aware of which Stream is actually powering your downstream experience. The first thing you might want to do is run:

```cli
yext streams list
```

This command will return **a table of the active Streams in your account**. Based on the information returned you should have a pretty good idea of which downstream experience a given Stream is powering. 

Now, say I recently made a configuration change within my downstream experience, for example, adding a field to a Streams Endpoint. I want to know whether the Streams endpoint has been updated according to my configuration change. I would run:

```cli
yext streams refresh status -s {streamId}
```

This command will provide the status of the most recent refresh on the specified Stream. 

If I wanted status information about previous refresh jobs, I could always run:

```cli
yext streams refresh list -s {streamId}
```

To list out all refresh jobs for a given Stream, then check the status of a specific refresh job using the refresh status command. 

Another thing I might want to do after making a configuration change is see what the format of the data is going to be with my updated configuration. I could run:

```cli
yext streams view records
```

Which would output the most recent records produced by Streams. 

If somehow I applied an invalid configuration (for example, a broken transform in a streams-endpoint configuration), I would see this failure when I ran refresh status on that Stream. Additionally, I would not see the complete new records being produced by the view records command. 
