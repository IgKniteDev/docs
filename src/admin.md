# Admin Control

This section will guide you through the different admin commands that you can use to control the bot.

## Overview

As a regular Discord user, you can easily go through the numerous commands using the slash (`/`) character, more notably, the "slash commands", and IgKnite is purposefully built this way to maintain a clean interface all the time.

But, if you are someone who is currently self-hosting the bot, you might sometimes need to have easy access to a handful of features such as loading and unloading a particular feature of the bot, shutting it down, checking its latency etc. This is where the admin commands come in.

## Prefix-based commands

The admin commands are not slash commands, but prefix-based commands. This means that you will have to type in a prefix before the command name to execute it. The default prefix for the admin commands is `.` and **can only be triggered by the bot owner**.

## Command list

Here is a list of all the admin commands that you can use:

- `.reloadext <extension_name>`: Reload a particular extension / cog of the bot.