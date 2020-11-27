======
Limits
======

Command
-------

+-------------------------------------------+--------------------------+---------------------------------------------------------+
| Command                                   | Permission               | Use                                                     |
+-------------------------------------------+--------------------------+---------------------------------------------------------+
| /mp limits                                | market.limits.see        | Let players see their limits                            |
+-------------------------------------------+--------------------------+---------------------------------------------------------+
| /mp limits get <uuid|name>                | market.limits.see_others | Let players (moderators) see other people limits        |
+-------------------------------------------+--------------------------+---------------------------------------------------------+
| /mp limits set <uuid|name> <amount>       | market.limits.edit       | Set the limits of a player (only database limits)       |
+-------------------------------------------+--------------------------+---------------------------------------------------------+
| /mp limits increment <uuid|name> <amount> | market.limits.edit       | Increment the limits of a player (only database limits) |
+-------------------------------------------+--------------------------+---------------------------------------------------------+
| /mp limits decrement <uuid|name> <amount> | market.limits.edit       | Decrement the limits of a player (only database limits) |
+-------------------------------------------+--------------------------+---------------------------------------------------------+

Systems
-------

In marketplace you can add limit of listings, there are 2 system that you can use

Permission-based limits
-----------------------
With this system (Selected by default) you can define permissions in your ``limits.permissions`` node in the config file, just like this

.. code-block:: yaml

   limits:
        permissions:
        - marketplace.limits.vip=3
        - marketplace.limits.donor=2

This mean that **ANY** player that has ``marketplace.limits.vip`` permission would have access to publish **3** listings

.. note:: You can add any permission name you want, not necessarily ``marketplace.*``
.. note:: Unlike database-based method, you can only use ``get`` command, if you want to manipulate the limits you should change the entire permission

What happend if i have multiple permissions?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can choose between two options on ``limits.multiple`` node in config file:

``stack`` (Selected by default) **Sum all the permissions you have**

``priority`` **Find the permission with more limits**

Database-based limits
---------------------
To enabled this mode you have to edit ``limits.mode`` node in your config to ``db`` instead of ``permissions``

This mode can be used by commands:

``/mp limits set <player> <slots>`` **Set the limits of a player (The player should be online!)**
``/mp limits get <player> <slots>`` **Get the limits of a player (The player should be online!)**
``/mp limits increment <player> <slots>`` **Increment the limits of a player (The player should be online!)**
``/mp limits decrement <player> <slots>`` **Decrement the limits of a player (The player should be online!)**

What method choose?
-------------------
This depends on what you wanna do, if you want to grant limits to a player for donating just use the permission-based system though if you want to grant different limits for each player for example buying in ingame store you should use the database-based system since is more practical for this kind of implementations

Default limits & Unlimited
--------------------------

Use ``limits.default`` node in config to define the default limit that a player have
And also you can use -1 limits to make it unlimited (Works in both systems and default in config)