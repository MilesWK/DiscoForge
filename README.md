[![DiscoForge](https://github.com/user-attachments/assets/bb1c86a3-59e2-46d1-b2eb-0f24374cc694)](https://github.com/MilesWK/DiscoForge/)
Create Discord Bots in Python quickly, with easy code!
[![PyPI version](https://badge.fury.io/py/DiscoForge.svg)](https://badge.fury.io/py/DiscoForge)
[![PyPI - License](https://img.shields.io/pypi/l/DiscoForge)](https://pypi.org/project/DiscoForge/)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/DiscoForge)](https://pypi.org/project/DiscoForge/)
[![PyPI status](https://img.shields.io/pypi/status/DiscoForge.svg)](https://pypi.python.org/pypi/DiscoForge/)


**Installation ⬇️**

Use `pip` to install the DiscoForge in the command prompt/terminal of your computer:
```bash
pip install DiscoForge
```
You can also use the `os` python module to install it: 
```python
import os

os.system("pip install DiscoForge")
```

**Quick Usage ⏩**

Wanna create a Discord bot with a REAL slash command, let's do it!

```python
import DiscoForge as ds # Import the "DiscoForge" module as "ds"

# Replace this with the token for your Discord bot.
Discord_bot_token = "<PUT-YOUR-DISCORD-BOT-TOKEN-HERE>"

bot = ds.discord_bot(Discord_bot_token) # Create the new discord bot instance

intents = bot.configure_intents(True, True, True) # Configure your bot intents
bot.create_bot(intents) # Create the bot

# Wanna slash command? Let's do it!

# Include the "interaction" here and define the function for your command
async def test_command(interaction):
    await ds.send_msg(interaction, "Hello,") # Send a message
    await ds.send_followup_msg(interaction, "World!") # You know what, that was fun. Let's send a follow up message!

# Register the command
command1 = ds.command() # Create a new command
command1.create_command("helloworld", "Hello World!", test_command, params=None) # Create the function with the name "helloworld" and using our "test_command" function.

# Just one last thing! Let's start the bot!
bot.start_bot() # Boom. We're done!
```

[Wanna learn how to do it ALL? Check out the wiki! (COMING SOON 😁)](https://github.com/MilesWK/DiscoForge/wiki)
