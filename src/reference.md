# Command Reference

IgKnite currently has more than 40 available bot commands, roughly distributed among four categories. All the commands are built on Discord's bleeding edge API and use the latest features.

The following is a list of all the available commands (updated: October 30, 2022).

## The Customization Commands
### /makerole [name] [color]
Creates a new server role with the specified *name* and *color*. Color is in hex.

| Parameter | Required | Default |
|---|---|---|
| name | Yes | |
| color | No | #000000 |

### /assignrole [member] [role]
Assigns a server *role* to the specified *member*.

### /removerole [role]
Removes a *role* from the server.

### /makeinvite [max_age] [max_uses] [reason]
Creates an invitation link to the server with the specified parameters.

| Parameter | Required | Default |
|---|---|---|
| max_age | No | 0 |
| max_uses | No | 1 |
| reason | No | No reason provided. |

### /nick [member] [nickname]
Changes the server *nickname* of the specified *member*

### /makechannel [name] [category] [topic]
Creates a new channel in the server with the given *name*, inside the given *category*, and sets the given *topic* to it.

| Parameter | Required | Default |
|---|---|---|
| name | Yes |  |
| category | No | None |
| topic | No | None |

### /makevc [name] [category]
Creates a new voice channel with the given *name* in the given *category*.

| Parameter | Required | Default |
|---|---|---|
| name | Yes |  |
| category | No | None |

### /makecategory [name]
Creates a new channel category with the specified *name*.

### /removechannel [channel]
Deletes the given *channel* from the server.

### /reset
Deletes all the messages from the current channel.


## The General Commands
### /avatar [member]
Displays your avatar or the avatar of the server *member* given.

| Parameter | Required | Default |
|---|---|---|
| member | No | You |

### /ping
Returns IgKnite's API response time, system latency, and uptime.


## The Moderation Commands
### /ban [member] [reason]
Bans the given server *member* for the given *reason*.

| Parameter | Required | Default |
|---|---|---|
| member | Yes |  |
| reason | No | No reason provided |

### /unban [member]
Unbans the given *member* from the server.

### /softban [member] [reason]
Temporarily bans the given *member* to delete their messages.

| Parameter | Required | Default |
|---|---|---|
| member | Yes |  |
| reason | No | No reason provided |

### /kick [member] [reason]
Kicks the given *member* from the server.

*Note: Kicked members can join the server again, but banned members can't.*

| Parameter | Required | Default |
|---|---|---|
| member | Yes |  |
| reason | No | No reason provided |

### /timeout [member] [duration] [reason]
Timeouts the given *member*.

| Parameter | Required | Default |
|---|---|---|
| member | Yes |  |
| duration | No | 30 seconds |
| reason | No | No reason provided |

### /purge [amount]
Deletes the given *number/amount* of messages in the channel.

| Parameter | Required | Default |
|---|---|---|
| amount | No | 1 |

### /ripplepurge [member] [amount]
Clears the messages sent by the given *member* if they fall in the given *index/amount*.

### /snipe
Recovers all the messages that were deleted/*sniped* in the last 25 seconds. *Neat, right?*

### /senddm [member] [msg]
Sends a message to the specified member's DM.

| Parameter | Required | Default |
|---|---|---|
| member | Yes | None|
| msg | Yes | None|

### /pins
Shows all the pins in the channel.

### /clearpins
Deletes/unpins all the pins in the channel.

### /pin [member]
Pins the last message by the mentioned *member*.

### /banword [words]
Bans the comma-separated *words*.

### /slowmode [seconds]
Enables slowmode in the channel and sets timeout to *seconds*. Set `0` in *seconds* to disable slowmode.


## The Inspection Commands
### /guildinfo
Shows all important information about the server.

### /userinfo [member]
Shows all important information on a user.

| Parameter | Required | Default |
|---|---|---|
| member | No | You |

### /roleinfo [role]
Shows all important information related to a specific role.

### /membercount [sticky]
Shows total number of members in channel and sidebar (if *sticky* is `True`).

| Parameter | Required | Default |
|---|---|---|
| sticky | No | `False` |

## The Music Commands
### /play [keyword]
Searches a soundtrack with the given *keyword* and adds it to the queue.

### /playrich [member]
Tries to enqueue a song from one's Spotify rich presence.

| Parameter | Required | Default |
|---|---|---|
| member | No | You |

### /pause
Pauses the currently playing song.

### /resume
Resumes the currently playing song.

### /stop
Stops playing the song and clears the queue.

### /join
Joins the VC you are in.

### /leave
Leaves the VC you are in (duh?).

### /volume [volume]
Sets the volume of the playing song. Just say `/volume 50`.

### /now
Displays an interactive control view for the current song.

### /skip
Vote to skip a song. The requester can automatically skip.

### /queue
Shows the player's queue.

### /rmqueue [index]
Removes a song from the queue at a given *index*.