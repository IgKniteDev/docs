# Command Reference

IgKnite currently has more than **48** available bot commands, roughly distributed among five categories. All the commands are built on Discord's bleeding edge API and use the latest features.

Legend: 
- `<required>` `[optional]` 

- 🔪 BotMod  

- ⚔️ BotAdmin

The following is a list of all the available commands (updated: December 15, 2022).

# ⚙️ General
### /avatar [member]
Displays your avatar / the avatar of a server member.
### /ping
Shows the bot's current response time and more.
### /help
Get to know more about IgKnite!
# 🔎 Inspection
### /guildinfo 🔪⚔️
Shows all important information about the server.
### /userinfo [member] 🔪⚔️
Shows all important information on a user.
### /roleinfo <role> 🔪⚔️
Shows all important information related to a specific role.
### /invites 🔪⚔️
Displays active server invites.
### /revokeinvites [member] 🔪⚔️
Revokes invites. By default this removes all invites but you can choose a server member.
### /audit [limit] 🔪⚔️
Views the latest entries of the audit log in detail.
# 🖌 Customization
### /makerole <name> [color] ⚔️
Create a new role.
### /assignrole <member> ⚔️
Assign a role to a server member.
### /removerole <role> ⚔️
Revome a role from the server.
### /makeinvite [max_age] [max_uses] [reason] 🔪⚔️
Create an invitation link to the server.
### /nick <member> <nickname> 🔪⚔️
Change nickname of a member.
### /makechannel <name> [category] [topic] ⚔️
Create a new text channel.
### /makevc <name> [category] ⚔️
Create a new voice channel.
### /makecategory <name> ⚔️
Create a new channel category.
### /removechannel <channel> ⚔️
Remove a channel from the server.
### /reset ⚔️
Resets the current channel.
### /afkvc [channel] [timeout] ⚔️
Configures the inactive (AFK) channel for the server.
# 🔨 Moderation
### /ban <member> [reason] 🔪⚔️
Bans a member from the server.
### /softban <member> [reason] 🔪⚔️
Temporarily bans members to delete their messages.
### /unban <member> 🔪⚔️
Unbans a member from the server.
### /kick <member> [reason] 🔪⚔️
Kicks a member from the server.
### /timeout <member> [duration] [reason] 🔪⚔️
Timeouts a member.
### /purge [amount] 🔪⚔️
Clears messages within the given index.
### /ripplepurge <member> [amount] 🔪⚔️
Clears messages that are sent by a specific user within the given index.
### /snipe 🔪⚔️
Snipes messages within 25 seconds of their deletion.
### /senddm <member> <msg> 🔪⚔️
Send DM to specific users.
### /pins
Shows all pinned messages in the current channel.
### /clearpins 🔪⚔️
Clears all pinned messages in the current channel.
### /slowmode <seconds> 🔪⚔️
Sets slowmode for the current channel.
### /banword <keywords> ⚔️
Add keywords to ban.
### /clearbannedwords ⚔️
Clears the list of banned keywords added by IgKnite.
### /showbannedwords ⚔️
Shows the list of banned keywords added by IgKnite.
### /clearnicks ⚔️
Clear everyone's nickname in the guild.
# 🎧 Music
### /play <keyword>
Enqueues playable stuff (basically sings you songs).
### /playrich [member]
Tries to enqueue a song from one's Spotify rich presence.
### /pause
Pause the currently playing song.
### /resume
Resume the currently playing song.
### /stop
Stops playing songs and clears the queue.
### /join [channel]
Joins the voice channel you're in. You can also specify which channel to join.
### /leave
Clears the queue and leaves the voice channel.
### /volume <volume>
Sets the volume of the current track.
### /now
Displays an interactive control view for the current song.
### /skip
Vote to skip a song. The requester can automatically skip.
### /queue
Shows the player's queue.
### /rmqueue <index>
Removes a song from the queue at a given index.