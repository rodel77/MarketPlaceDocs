=============
Purge Command
=============

With purge commands, you can clear unused data, remove all listings of a player or remove all the listings

Command Syntaxis
================

/market purge <argument-name> [argument-value]

Arguments & Examples (Read all before executing any purge command)
=========

These arguments will remove ANY listing published 1 year ago

``/market purge -t 360d``

As you can see it says -t "Time" 360 Days you can use d (Days) h (Hours) m (Minutes) s (Seconds) and you can multiple units ex: "23d40h20m18s" or "900m" etc but notice that will make players that has items published in marketplace lose it

Then you can remove only history with this command: (Items that are sold and claimed unused data, its just there to show when players search their old purchasese/sales)

``/market purge -h -t 360d``

Now you are clearing the history of 1 year ago

.. note:: Its recommended to purge history data if you have to much players publising items or just a cheap db

As well you can remove the time argument to remove all history data

``/market purge -h``

You can also remove all the listings in the marketplace (This will truncate the db table)

``/market purge -all``

Specifyng Users
---------------

To remove all data of a specific seller you can use this command:

``/market purge -s rodel77``

This will search the last name registered in the db but players can change the name then you can use uuid:

``/market purge -s 658f236d-5ecc-49d4-b074-4161ebff9117``

You can also mix this with the command showed above to delete listings of time ago

``/market purge -s 658f236d-5ecc-49d4-b074-4161ebff9117 -t 306d``

Or just clear the history of the player

``/market purge -s 658f236d-5ecc-49d4-b074-4161ebff9117 -h``

Or clear the history of 1 year ago

``/market purge -s 658f236d-5ecc-49d4-b074-4161ebff9117 -h -t 306d``

As well you can specify the buyer

``/market purge -b <uuid or name>``

And remove purchases specifyng the buyer and the seller

``/market purge -b buyer -s seller``

Or the history

``/market purge -b buyer -s seller -h``

.. note:: When you perform the command he's going to tell you what he's going to do (Any question please join in the discord support chat and ask to rodel before experimenting!)