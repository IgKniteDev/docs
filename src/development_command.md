# Adding commands

Have an idea? Let's build it! <br>

## Note

It's noteworthy that your contributions must follow the [Code of Conduct](https://github.com/IgKniteDev/IgKnite/blob/main/CODE_OF_CONDUCT.md) included with the repository. Make sure to read it before creating any unnecessary changes within the code. We'd love to see your ideas come to life within IgKnite! <br>

## The Steps

In order to add new commands to the project, you must follow through the three mandatory steps mentioned below: <br>

### 1. Choosing a "Cog"

On both [discord.py](https://github.com/Rapptz/discord.py) and [disnake](https://github.com/DisnakeDev/disnake), categories of commands are referred to as "cogs". There are six different cogs which come built-in with IgKnite located in the **cogs** subdirectory. Navigate to your chosen one and have a look at the source code before making any changes. <br>

### 2. Creating the command

Once you have decided which cog to add your command to, we can start writing some code now!

Discord has three types of commands:

- **Slash commands** can be used by pressing `/` and then typing the command.
- **User commands** can be used by right-clicking on a user's avatar and then selecting 'Apps'.
- **Message commands** are similar to user commands but need you to click on a message instead of someone's avatar.

Below is an example of a very basic slash command which greets a server member. You'll be using such syntax in most of your commands.

```python
# sample imports
import disnake
from disnake.ext import commands
from disnake.ext.commands import Param  # used for options

# the cog
class SomeCog(commands.Cog):

...

	@commands.slash_command(
		name='greet',
		description='Greets a member!',
		dm_permission=False  # disables the command inside DMs
	)
	async def _greet(
		self,
		inter: disnake.CommandInteraction,
		member: disnake.Member = Param(description='Mention the server member.')
	) -> None:
		await member.send(
			f'Hey there! Welcome to {inter.guild.name}.'
		)
```
<br>

On the other hand, you can also write code and deploy to all three types of commands at once! In the example given below, we've tried to make a ban command that uses the very same logic for deploying itself in three forms:

```python
# Backend for ban-labelled commands.
# Do not use it within other commands unless really necessary.

async def _ban_backend(
	self,
	inter: disnake.CommandInteraction,
	member: disnake.Member,
	reason: str = 'No reason provided.'
) -> None:
	await inter.guild.ban(
		member,
		reason=reason
	)
	await inter.send(f'Member **{member.display_name}** has been banned! Reason: {reason}')


# ban (slash)
@commands.slash_command(
	name='ban',
	description='Bans a member.',
	dm_permission=False
)
@commands.has_any_role(LockRoles.mod, LockRoles.admin)
async def _ban(
	self,
	inter: disnake.CommandInteraction,
	member: disnake.Member = Param(description='Mention the server member.'),
	reason: str = Param(
		description='Give a reason for the ban.',
		default='Default reason.'  # having a default value makes it optional
	)
) -> None:
	await self._ban_backend(inter, member, reason=reason)


# ban (user)
@commands.user_command(
	name='Ban',
	dm_permission=False
)
@commands.has_any_role(LockRoles.mod, LockRoles.admin)
async def _ban_user(
	self,
	inter: disnake.CommandInteraction,
	member: disnake.Member
) -> None:
	await self._ban_backend(inter, member)


# ban (message)
@commands.message_command(
	name='Ban',
	dm_permission=False
)
@commands.has_any_role(LockRoles.mod, LockRoles.admin)
async def _ban_message(
	self,
	inter: disnake.CommandInteraction,
	message: disnake.Message
) -> None:
	await self._ban_backend(inter, message.author)

...
```
<br>

### 3. Test and deploy

Once you are done making your changes, push them to your fork and create a valid pull request. [Here's](https://github.com/IgKniteDev/IgKnite/pull/221) an example pull request which you can have a look at to learn about the pattern.

The pull request must pass the given workflows (the ones mentioned earlier) and receive a green 'check' symbol to qualify for a merge. We hope you'll do your best to gain it!