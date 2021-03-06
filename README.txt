﻿This lightweight data pack is designed to make your old worlds feel new again
by instantly dropping you off in some (potentially) far-flung corner of the map
with no indication of where you've ended up. 

Will you find your way home again? Or make a new one?

Instructions:

Once the .zip file (containing the 'data' directory and 'pack.mcmeta' file)
has been placed in the datapacks folder of your world, it's good to go,
and doesn't do anything until you ask it to.

To be instantly teleported along a random vector in the overworld,
simply enter the command:

/function fresh_start:begin


...and you're falling out of the sky up to 10 000 blocks away from where you started.
(by default -- it can be configured either by command or by editing the files).
Don't worry, you've got 15 seconds of invulnerability to help you land on your feet.

To set your spawn point here, enter:

/function fresh_start:accept


That's it!


============== CONFIGURE SETTINGS ===============

#max -- determines the maximum distance a player can be teleported from their
starting position along each of the x & z axes. [10000 by default]

#min -- specifies the minimum distance you'll be transported, calculated as the crow flies;
the algorithm will generate random points until it finds one that's far enough away. [default 0]


To adjust settings without changing any source code, run the following commands:
First:

/function fresh_start:config_add	(this is necessary to store the config data)


To set the MAXIMUM teleport distance for each axis, enter:

/scoreboard players set #max fsconfig <value>


To set the MINIMUM distance from the starting point:

/scoreboard players set #min fsconfig <value>


(**note: the minimum distance describes a circle centred on the starting point,
while the maximum defines a square area. therefore, if #max and #min are equal,
the resulting location will be forced into the corners of the square)


To remove the scoreboard objective, run the command:

/function fresh_start:config_clear


Alternatively, the maximum and minimum can be changed at the source in the file:

data\fresh_start\functions\settings\config.mcfunction	(can be opened with any text editor)


=================== CREDITS =====================

This data pack makes use of the linear congruential pseuso random number
generator developed by mcskware (aka AspiringIdiot on reddit), the source
of which can be found at https://github.com/mcskware/prng

It is entirely unchanged here apart from my having removed the file tagging its
functions in minecraft:load

This is my first attempt at playing with commands in Minecraft, so if any
of the design or syntax seems daft that's probably why. If there's anything huge I've missed,
feel free to give me a shout over on reddit.


almostambidextrous
May 2019

https://www.reddit.com/r/Minecraft/comments/bp5ezx/i_made_a_data_pack_113_teleport_to_a_random/
