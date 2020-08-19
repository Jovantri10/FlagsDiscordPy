``` python
 © Jovantri Immanuel Gulo
```
# Require
### discord.py
> 1.4.1
### python
> 3.8

# Upgrade Discord.py
``` bash
pip install discord.py --upgrade
```
or, uninstall and install manual `discord.py` module
# Examples
### cogs/userinfo.py
> if u using cogs, u can use this
``` python
import discord
from discord.ext import commands

class Userflags(commands.Cog):
    
    def __init__(self, bot):

        self.bot = bot     

    @commands.command()
    async def userflags(ctx):
      u = ""
      p = ctx.author.public_flags
     if p.hypesquad_brilliance:
       u += "INPUT_EMOJI_BRILLIANCE_FLAGS"
     if p.hypesquad_bravery:
       u += "INPUT_EMOJI_BRAVERY_FLAGS"
     if p.hypesquad_balance:
       u += "INPUT_EMOJI_BALANCE_FLAGS"

     flagsembed = discord.Embed(title="User Flags {}".format(ctx.author.mention))
     flagsembed.add_field(name="{} flags".format(ctx.author.mention), value="u")
     await ctx.send(embed=flagsembed)

def setup(bot):
  bot.add_cog(userflags(bot))
```
