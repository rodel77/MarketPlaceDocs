========
Commands
========

Information about the commands

+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| Command                                                   | Permission                                  | Recommended Rank | Description                                                              |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp publish/sell <price>                                  | market.publish                              | Users            | Sell the item in your hand.                                              |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp search                                                | market.search                               | Users            | Open the search menu.                                                    |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp my/self                                               | market.my                                   | Users            | Open your "dashboard".                                                   |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp listings/inspect <playeruuid/playername>              | market.listings                             | Moderators       | Open the "dashboard" of another player (You can delete items).           |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp purge <parameters>                                    | market.purge                                | Moderators       | Purge listings with specific parameters.                                 |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp reload                                                | market.reload                               | Admins           | Reload the plugin configuration.                                         |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp limits [get|set|increment|decrement] [player] [slots] | Check: :doc:`../misc/limits`                | Admins & Players | Manage the limits of players.                                            |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp select <parameters>                                   | market.select                               | Moderators       | Get a plain chat message of specific listings (Same parameters as purge).|
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp help [command]                                        | (No permission required)                    | Users            | Open the help menu or get help from a specific command.                  |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp cancel/borrow <options>                               | market.cancel                               | Moderators       | Cancel items, for now just --all enabled (Experimental/Migration).       |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp setpin/webpin <new-pin>                               | market.setpin                               | Users            | Sets the pin of your webclient account. WebMarket should be enabled.     |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp wallet/webmoney <deposit/widthdraw/check> [player/$]  | market.wallet                               | Users            | Manage the money in your webclient account. WebMarket should be enabled. |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp migrate                                               | market.migrate                              | Admins           | Used to migrate from other plugins similar to MP. (Requests Open).       |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+
| /mp migrate-nbt                                           | market.migrate-nbt                          | Admins           | Used to migrate from SNBT to NBT (Update 3.0.0).                         |
+-----------------------------------------------------------+---------------------------------------------+------------------+--------------------------------------------------------------------------+

Contents
========

.. toctree::
    :maxdepth: 2
    :titlesonly:

    purge
