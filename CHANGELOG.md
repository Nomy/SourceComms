#Changelog
* **0.9.263** - Fixed SourceComms_SetClientMute params description. Thanks to [Bara](https://github.com/Bara20).
* **0.9.262** - Fixed plugin include file to prevent compiling errors when twice included.
* **0.9.260** - Added Deutsch translation. Thanks to [winter](http://steamcommunity.com/profiles/76561198012507628).
* **0.9.259** - Fixed bug with loading issuer admin's authid.
* **0.9.257** - Fixed bug (creating unused file `%s is gagged from web` on server) with logging gags from web. Thanks to [reji](https://forums.alliedmods.net/member.php?u=235571).
* **0.9.256**
    * Added Portuguese (Brazilian) translation. Thanks to [StayOx](https://forums.alliedmods.net/member.php?u=185412).
    * Removing quotes and whitespaces from reason.
    * Fixed reason loss in ungag/unmute console commands.
    * Fixed wrong fail state messages.
    * Fixed memory leak in unblock function.
    * Fixed bug with showing "unblocked" message if player wasn't unblocked.
* **0.9.242** - Fixed bug with removing temporary punishments by admins without special flag and greather immunity level. Thanks to [White Wolf](http://hlmod.ru/forum/member.php?u=10428) for reporting and fix testing.
* **0.9.233**
    * Added ability to use @all, @blue, @ct, etc. as punishment target (without saving to DB).
    * Added ability to temporary mass-removing punishements (with @all, @blue, @ct, etc targets) - without removing from DB.
    * Fixed bugs with permissions check on removing punishments.
    * Fixed bug with unsilence on players which has combination of temp and time/perm punishments.
    * Fixed [bug](https://bugs.alliedmods.net/show_bug.cgi?id=5786) with broken mysql connection encoding after reconnect. Supported on SM builds greather than **1.6.0-dev+3947**.
    * Now plugin uses common sourcemode logs for errors and messages. You can delete sourcecomms.log file from your sourcemod logs folder.
    * Removed ServerID auto-detection. You must specify it in the sourcebans config.
    * Some bugs fixes.
    * Code improvements.
* **0.9.9** - Added Polish translation. Thanks to [killerps](https://forums.alliedmods.net/member.php?u=145192).
* **0.9.7** - Added the ability to use the player's name in quotes in console commands. Request from [lyric](https://forums.alliedmods.net/member.php?u=197409).
* **0.9.1**
    * Plugin was approved! Many thanks to [alongub](https://forums.alliedmods.net/member.php?u=58635).
    * No changes were made, only version bump.
* **0.8.257**
    * Now already punished players are hided from menu. Thanks for idea to [wingblack](https://forums.alliedmods.net/member.php?u=219943).
    * Allowed to use serverID = 0. Request from [bottiger](https://forums.alliedmods.net/member.php?u=101497).
* **0.8.253**
    * A lot of code was refactored.
    * Added *Servers White List* feature. More details in README.
    * Fixed console immunity value for punishments received from web.
    * Added **natives** for plugin developers. More details in README.
    * Fixed bug with unblocking commands, if they were called by console.
* **0.8.158**
    * Fixed `Unknown command` reply in client console.
    * Fixed/added SQL-escaping to prevent SQL-injections.
    * Changed way of connecting to database, added checking for *connection lost*.
    * Fixed bug with unicode symbols in entries from queue.
    * Fixed bug with only one punishment per steam-id could be saved in queue.
    * Fixed bug with `MaxLength` checking, which doesn't work correctly for admins with `UNBLOCK_FLAG`.
    * Some optimizations of SQL-queries.
    * Improved plugin state *consistency* with unstable database connection.
    * Other code improvements. Thanks to [alongub](https://forums.alliedmods.net/member.php?u=58635).
* **0.8.89** - Fixed bug with MaxLength checking in console commands.
* **0.8.88**
    * Added `MaxLength` option to config. See plugin config for mor details.
    * Fixed admin immunity determination in sql queries.
    * Added setting up console immunity on block fetching.
* **0.8.79** - Added colored prefix to all output messages.
* **0.8.75**
    * Code improvements.
    * Fixed some mistakes in actions logging.
* **0.8.65**
    * Code improvements.
    * Fixed bug with unicode arguments in punishment commands.
    * Added command `sm_comms` for players, which provides viewing communications status of himself.
    * Bots are now removed from menu targets list.
* **0.8.1**
    * Fixed bug with *player's name in the database sometimes was a part of another "sql-query"*
    * Code improvements to avoid similar bugs in the future.
    * Disabled sql-queries log.
* **0.7.122**
    * Fixed bug: punishments were recorded into the database twice.
    * Removed "select from queue" query from logging.
    * Fixed bug with wrong logging comms actions in SM logs.
    * Enabled sql-queries log.
* **0.7.114**
    * Fixed some flaws in the sql queries.
    * Small code improvements.
* **0.7.111** - First release on AlliedMods.
* **0.7.97**
    * Minor bugs fixed.
    * DEBUG info now disabled by default.
    * Now plugin is "beta".
* **0.7.60**
    * Changed internal data structure.
    * Added to Menu List of Current players punishments (from original ExtendedComms plugin).
    * Added "ConsoleImmunity" and "DisableUnblockImmunityCheck" variables to config.
* **0.6.52**
    * Now plugin will auto-reloads after update.
    * Little changes in translation.
* **0.6.51** - Added temporary punishments.
* **0.6.44** - Added "DefaultTime" variable to config.
* **0.6.42** - In debug mode, text of all sql queries will stored in separate log.
* **0.6.37** - Added console commands that provides unblocking player comms via web.
* **0.6.34** - Added Updater support.
* **0.6.20** - Fixed bug: "after restoring a database connection expired punishments were not added to main database".
* **0.6.19** - Fixed bug with displaying admin activity after restoring a database connection, but not immediately.
* **0.6.14** - Added console commands that provides blocking player comms via web.
* **0.5.30** - First public alpha.
