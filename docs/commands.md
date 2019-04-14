New commands are one of the huge additions to the user-experience. We added over 40 additional commands, which are explained below. (In alphabetical order)
You will find a list of all the commands included with the plugin, along with a detailed description of their usage and purpose.

??? tip "Tab-Completion available with [BeezigForge](index.md#beezigforge-extension-for-forge)!"
    Most commands feature tab-completion, which lets you easily enter names or other values. Still, this feature will require the [BeezigForge](index.md#beezigforge-extension-for-forge) addon!


****

## All commands

??? abstract "This list is valid for `Beezig 6.0`"
    If you are playing on another version, this information may have changed. Run [`/beezig`](#beezig) to get your version.

??? tip "All 'game' or 'mode' terminology used requires the shortcode of the game to be used."
    Example: `TIMV`, `BED`, `DR`, `SKY`, `BP`, `HIDE`

??? tip "For chat setup, most maps are specified in the format `mode_map` & Spaces are replaced with `_`. Special characters (colons etc.) must still be added!"
    Example: `/autovote add TIMV_Hermit_Sands:_Classic`

    Example: `/autovote add timv_mineville:_classic`

!!! info "`[param]` is a mandatory parameter, while `(param)` is optional."


****

### AddNote <small>`TIMV`</small>
Adds a small text note to your Trouble in Mineville notepad, viewable by [/notes](#notes-timv).

- Syntax: `/note [note]`
- Alias: `/note, /addnote`


****

### AutoGG
If [enabled](settings.md#general), you will automatically say gg at the end of a game. You can customize the text, delay and which games to use on. Run `/autogg` to see current status. **More info on AutoGG on the [features page]()!**

- Syntax: `/autogg`
- Syntax: `/autogg [text/delay] [value]`
- Syntax: `/autogg [enable/disable] [shortcode]`


****

### AutoVote
Manges the autovoter.
If [enabled](settings.md#general), we will automatically vote for your favorite maps when you join a lobby. Your favorites are listed via the `list` argument. Add favorite maps with `add/remove`. After we checked the voting options, we'll go through your favorites top to bottom, meaning the top map will be checked first. To reorder your maps, use the `place` argument. **More info on Autovote on the [features page]()!**

!!! info "If you have [BeezigForge](index.md#beezigforge-extension-for-forge), everything will be done through a GUI instead of chat. Run `/autovote`"

- Syntax: `/autovote`
- Syntax: `/autovote list [mode]`
- Syntax: `/autovote [add/remove] [map]`
- Syntax: `/autovote place [map] [newPosition]`
- Alias: `/autovote, /avote`


****

### Beezig
This command will get you information on your current Beezig installation (Version, Client)
It will also indicate if a update is available.
The `commands` argument will instead print all loaded commands.

- Syntax: `/beezig`
- Syntax: `/beezig commands`
- Syntax: `/beezig reconnect`


****

### BeezigParty
Asks the current online Beezig users to join your party. `search` requests a party; `amount` is the amount of players needed. The second parameter specifies the reason of the party. Accept the party by using the exact name of the requester.

- Syntax: `/bparty search [amount] (reason)`
- Syntax: `/bparty accept [player]`

??? example
    Example: `/bparty search 1 BedWars Duos`

    Example: `/bparty accept ItsNiklass`


****

### BestGame
Calculates which gamemode the most played gamemode is. Use this to find out 'what is their main game?'. This is calculated by using the average top 20 points and comparing it to their points. To get the full list of games, add a second argument (anything).  When no `player` is specified, your stats are calculated.

!!! bug "TIMV & OITC are currently not calculated/considered! `Beezig 6.0-pre`"

- Syntax: `/bestgame (player) (*)`
- Alias: `/bestgame, /bg, /maingame`


****

### Blockstats <small>`HIDE`</small>
Prints a list of the levels of all hiding-blocks by the player, sorted by total experience. When no `player` is specified, your stats are calculated.

- Syntax: `/blockstats list (player)`
- Alias: `/blockstats, /bs`


****

### ChatReport
Beezig will connect to the Hive Report system and will automatically file a chat-report from ingame. When you run the command, a chatlog will be generated and the report form will be filled. **More info on ChatReport on the [features page]()!**

!!! warning "This feature only works on the 5zig version. LabyMod handles ChatComponent packets differently."

??? tip "Only the official chat-report-reasons, as seen on the report form, are valid."
    A list of available reasons will be printed in case of a invalid reason.


- Syntax: `/chatreport [player] [reason(s)]`
- Alias: `/chatreport, /reportchat`


****

### CheckPing
Find out the ping of a player.  When no `player` is specified, your ping is shown. The latency is returned in milliseconds.

- Syntax: `/checkping (player)`
- Alias: `/checkping, /cping`


****

### ClosestToWR <small>`DR`</small>
Print information on how PB's relate to WR's and what the difference is. So it shows `player`'s best and worst DeathRun times according to the difference between them and the respective World Records. Either prints best, worst and average, or all played maps (extended) with a second argument (anything). When no `player` is specified, your stats are calculated.

- Syntax: `/cwr (player) (*)`
- Alias: `/cwr, /bestmap`


****

### CustomTest <small>`TIMV`</small>
Manages the custom test messages for Trouble in Mineville. Use `add/remove` to change your custom list. There are predefined ones. Use `list` to list all messages. "{p}" will serve as the player.

!!! info "If you have [BeezigForge](index.md#beezigforge-extension-for-forge), everything will be done through a GUI instead of chat. Run `/customtest`"

**More info on Custom test messages on the [features page]()!**

- Syntax: `/customtest [add/remove] [message]`
- Syntax: `/customtest list`
- Alias: `/customtest, /ctest`

??? example
    Example: `/customtest add Please go into the tester, {p}!`


****

### Daily
Print information on daily points. **More info on Daily Points on the [features page]()!**

- Syntax: `/daily (mode)`


****

### DeathrunRecords <small>`DR`</small>
Shows the DeathRun kills and deaths records for `player` on the specified `map`.

- Syntax: `/drbest (player) (map)`
- Alias: `/drbest, /drrec`


****

### Leaderboard
Fetches leaderboard data from the API and print a nice leaderboard. This shows main points, rank and network rank. If no `mode` is specified, the currently played game will be used. Both `startPos` and `endPos` serve as inclusive.
**More info on Leaderboards on the [features page]()!**

- Syntax: `/lb [startPos] [endPos] (mode)`
- Alias: `/lb, /leaderboard, /leaderboards`


****

### Math
With the command you can execute arithmetical expressions in your Minecraft instance. Basic operations are supported, but also roots, powers and more - a small quick calculator. You can only invoke methods from the Math class.

- Syntax: `/math [expression]`

??? Example
    **Basic operations are supported, for example:**

    * `/math 5+3` returns `8`;
    * `/math 5-3` returns `2`;
    * `/math 5*3` returns `15`;
    * `/math 5/3` returns `1.66666666667`.

    However, you can do much more.
    What you're writing in the expression is **pure JavaScript** so you can make use of the **Math** helper class.
    So, for example:

    * `/math Math.sqrt(9)` returns `3` (Square Root);
    * `/math Math.pow(10, 3)` returns `1000` (10 to the power of 3).

     All the supported Math operations can be found [here](https://www.w3schools.com/js/js_math.asp).

****

### Medals
Simply show the amount of medals of `player`. When noone is specified, yours are shown.

- Syntax: `/medals (player)`


****

### MessageOverlay
Allows you toggle private messages to `player`, just like `/p` does for parties.
Just running `/msg [player]` will toggle the private message mode to `player`. All your normal messages will get sent in private to `player`. Doing just `/msg` will stop automatically sending.

- Syntax: `/msg`
- Syntax: `/msg [player]`
- Alias: `/msg, /tell`


****

### Monthly

Returns what player is on `position` on the monthly leaderboards of `game`. Additional stats like points and calculations are also shown. If no `mode` is specified, the current game will be used.

**More info on Monthly on the [features page]()!**

- Syntax: `/monthly [position] (mode)`

!!! info "Use /records (Advanced Records) to find out a players rank."

****

### Notes <small>`TIMV`</small>

Prints out all notes saved in the current TIMV game via [`/note`](#addnote-timv)

- Syntax: `/notes`

****

### PB <small>`DR`</small>

Shows the personal best/fastest time time of `player` on `map`. Noting specified means your stats on the current map will be calculated. If no `map` is specified, the current active map will be used (if available).

- Syntax: `/pb (player) (map)`

****

### PlayerStats

Ranks all the players in your lobby/hub by the points in the game you specified. This will be returned like a leaderboard of your server and makes it easy to indentify the top players in your game (It may take a few seconds!).
If no `mode` is specified, the current game will be used.
By default, the main points `stat` is used. Usually, you can try all `stat`'s listed on /records. (All available stats are tab-able with [BeezigForge](index.md#beezigforge-extension-for-forge))

- Syntax: `/playerstats (mode) (stat)`
- Alias: `/playerstats, /ps`

??? Example
    Example: `/ps timv karma/rolepoints`

****

### Ranks

This will print all available ranks and required points for `game`. (Stored internally!)
If no `game` is specified, the current game will be used.

- Syntax: `/ranks (game)`

****

### ReVote

This command will retrigger the [autovote]() process in your lobby and is used, for example, after editing favourite maps.

 - Syntax: `/revote`
 - Alias: `/revote, /rev`

****

### Report

This command allows you to report other players to the moderators, as a test. It will alert all moderators on the [Hive Unofficial Discord](https://discord.gg/q4mAbPK) as well as notifying all moderators using Beezig in their chat. Obviously, as a moderator using Beezig, this feature can be turned off using [/settings](#settings) ([`MOD_REPORT_NOTIFICATION`](settings.md#general)). **More info on Reports on the [features page]()!**

!!! warning "On abuse, your permissions may be revoked."

!!! info "You must wait 30 seconds between reports."

!!! info "This is not the proper way to report chat offences with Beezig. Please use [/chatreport](#chatreport) instead."

If the player is offline, you will be required to confirm the username.

You can specify multiple `players` at once. Splilt them by using `", "`.
Additionally, you can submit any `reason` you want.

- Syntax: `/report [player(s)] [reason(s)]`

??? Example
    Example: `/report RoccoDev, ItsNiklass AntiKnockback, Kill Aura`

***

### Rig

Joke command for lucky crates.

 - Syntax: `/rig`

****

### Say

Beezig's commands automatically have priority over Hive's commands. If for whatever reason we are accidentally overwriting a (new) Hive command, you can use this to except your `command` from our system.

 - Syntax: `/servercommand [command]`

****

### Seen

Shows either when the `player` was last seen, or in which game the `player` is, just like on the Hive website.

 - Syntax: `/seen [player]`

****

### Settings

!!! info "This description is only for 5zig without [BeezigForge](index.md#beezigforge-extension-for-forge) - See [Settings.](settings.md)"

**Manages Beezig's settings.**

Using `list` prints all available settings with their value and description, similar to [Settings.](settings.md#all-settings) With `filter [gamemode]` you can filter the huge list to only return specific settings. To change your settings, insert `setting` and enter either `true` or `false`. Make sure to fully type out the setting. (Case-Insensitive!)

 - Syntax: `/settings list`
 - Syntax: `/settings filter [gamemode/global]`
 - Syntax: `/settings [setting] (true/false)`

??? Example
    Example: `/settings autovote_random false`

****

### Shrug

¯\\\_(ツ)\_/¯
Fun command. Either sends the shrug emote or appends it to `message`.

 - Syntax: `/shrug (message)`

****

### Tokens

Simply show the amount of tokens of `player`. When noone is specified, yours are shown.

- Syntax: `/tokens (player)`

****

### UUID

Shows the UUID of `player`. If `c` is present, the UUID will be copied to your clipboard.

- Syntax: `/uuid [player] (c)`

****

### Uptime

Shows how long you have been on Hive. Additionally shows the time you have been in your party.

- Syntax: `/uptime`

****

### Volume <small>BP</small>

Allows you to toggle the volume of Beezig's internal BP jukebox between 0% and 100%. (35% is recommended). **More info on the Jukebox on the [features page]()!**

- Syntax: `/volume [0-100]`
- Alias: `/volume, /vol`

****

### WR <small>DR</small>

!!! warning "Outdated Java! - If you have received a warning on startup & this does not work: [How to fix.](javaerror.md)"

Displays the world record (fastest time on [speedrun.com](https://www.speedrun.com/mcm_hivemc)) on the named `map`.
If no `map` is specified, the current map will be used.

- Syntax: `/wr (map)`

****

### Winstreak

Gives you information about your current/best winstreak in `mode`.
If `mode` is not specified, the current mode will be used.

- Syntax: `/winstreak (mode)`
- Alias: `/winstreak, /streak`

****

### ZigCheck

Checks if `player` has once in their lifetime launched 5zig. Not if he is currently using 5zig!

If you instead of a player, specify `-a` **all** players in the current lobby will be checked (Similar to [`/ps`](#playerstats)).

- Syntax: `/zig [player/-a]`
- Alias: `/5zig, /zig`

****
