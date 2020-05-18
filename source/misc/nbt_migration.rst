================
SNBT -> NBT Migration
================

MarketPlace was using SNBT (String NBT) to save item data but since 3.0.0 we are going to use Binary NBT, this requires a migration process.

This might seem useless but otherwise, there's a huge chance that your whole MP catalog will not work in future versions.

Why the migration
=================

Minecraft String NBT system is inconsistent, just look at this test that I did:

+ 1.7.10: ``{pages:[0:"This is the body part 1",1:"This is the body part 2",],author:"rodel77",title:"This is the titl",}``
+ 1.8.8:  ``{pages:[0:"This is the body part 1",1:"This is the body part 2"],author:"rodel77",title:"This is the titl"}``
+ 1.9.4:  ``{pages:[0:"{\"text\":\"This is the body part 1\"}",1:"{\"text\":\"This is the body part 2\"}"],author:"rodel77",title:"This is the titl",resolved:1b}``
+ 1.10.2: ``{pages:[0:"{\"text\":\"This is the body part 1\"}",1:"{\"text\":\"This is the body part 2\"}"],author:"rodel77",title:"This is the titl"}``
+ 1.11.2: ``{generation:0,pages:[0:"{\"text\":\"This is the body part 1\"}",1:"{\"text\":\"This is the body part 2\"}"],author:"rodel77",title:"This is the titl",resolved:1b}``
+ 1.12.2: ``{generation:0,pages:["{\"text\":\"This is the body part 1\"}","{\"text\":\"This is the body part 2\"}"],author:"rodel77",title:"This is the titl",resolved:1b}``
+ 1.13.2: ``{generation:0,pages:["{\"text\":\"This is the body part 1\"}","{\"text\":\"This is the body part 2\"}"],author:"rodel77",title:"This is the titl",resolved:1b}``
+ 1.14.4: ``{generation:0,pages:['{"text":"This is the body part 1"}','{"text":"This is the body part 2"}'],author:"rodel77",title:"This is the titl",resolved:1b}``
+ 1.15.2: ``{generation:0,pages:['{"text":"This is the body part 1"}','{"text":"This is the body part 2"}'],author:"rodel77",title:"This is the titl",resolved:1b}``

As you can see this doesn't make any sense because:

+ Imagine you are in 1.8.8, then you can't update to 1.9.4 for the fact that your SNBT is invalid
+ MarketPlace-WebClient uses regex so reading "pages", for example, will yield ``text`` of ``0:`` depending on the MC server

With these change we cannot guarantee that items will work forever in any given version, NBTS **CONTENT** can change, but structure didn't since 2011 and there's no chance of doing so.

After doing tests with GZIP-Compressed Binary NBTS (parsing the binary in each version and again) I can tell that they are all the same; deterministic.

How to do it?
=============

If you just downloaded the plugin and made a few tests just delete the tables, that would be the best, new tables will generate with new NBTS.

Otherwise you would like to backup your ``catalog`` table first (in SQLite just copy the .db file, in MySQL you can export the SQL Migration).

Then you can run ``/mp migrate-nbt``, this will disable the MarketPlace for obvious security reasons and might take a while (you will be told the current percentage, each 10%). I don't really recommend stopping the server but is not a mortal thing to do (you'll have to start the whole process).

After the migration is completed only people with ``marketplace.post-migration`` permission will be able to use the MarketPlace, this process allows you and other OPs to check that everything is okay (it should be if all of your items where created in the same version as you run this command).

To leave everything just like before use ``/mp migrate-nbt`` again, now all the users with access to the marketplace can enjoy it again.

**I am not resposible for data-loss in case you haven't made a backup**

You can report any other issue to me, please grant as much info as possible.