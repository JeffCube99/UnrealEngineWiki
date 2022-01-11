UI Quick Reference
==================

Tables
------

*   `UE4 Tables and Widgets Reordering Tutorial <https://youtu.be/d8Tr4miGP_w>`_
*   `UE4 Online Subsystem <https://docs.unrealengine.com/en-US/ProgrammingAndScripting/Online/index.html>`_
*   `UE4 Online Subsystem Steam <https://docs.unrealengine.com/en-US/ProgrammingAndScripting/Online/Steam/index.html>`_
*   `More Comprehensive Multiplayer Tutorial <https://www.youtube.com/watch?v=ngBI40tjirE&ab_channel=UnrealEngine>`_

Materials
---------

*   `Striped Materials <https://youtu.be/fITAkG3_qP8>`_
*   `Varying Materials With Time <https://youtu.be/SMQI9_MEfRM>`_
*   `Vertex Painting <https://youtu.be/oCWcH_Mktz8>`_
*   `Sprite Materials <https://docs.unrealengine.com/en-US/AnimatingObjects/Paper2D/Sprites/index.html>`_
*   `Ripple Effect <https://www.youtube.com/watch?v=jOpmlaDekcc>`_
*   `Two Sided Material <https://www.youtube.com/watch?v=s5qv0YBCE88>`_

Notes
^^^^^

*   Solution for future generations: Sprites must be marked as 'Movable' if you want to change their color.
    `link <https://www.reddit.com/r/unrealengine/comments/4hsnhd/setting_sprite_color_not_working/>`_


Multiplayer
-----------

*   `Local Multiplayer Spawning System <https://youtu.be/3lN2eZIgAQ0>`_

..  note::

    When dealing with server client multiplayer the local player index is always 0

*   `UE4 Mulitplayer Blueprint Series <https://youtube.com/playlist?list=PLZlv_N0_O1gYqSlbGQVKsRg6fpxWndZqZ>`_
*   `UE4 Network Compendium <https://cedric-neukirchen.net/Downloads/Compendium/UE4_Network_Compendium_by_Cedric_eXi_Neukirchen.pdf>`_

Replication
^^^^^^^^^^^

*   Setting Replication to reliable should be for essential functions, not things like particle effects. Your network
    can get bogged down if too many things are set to be reliable
*   Player Controllers Exist both on the client and the server. There are 2 versions of them. One that exists on the
    server and the one that exists on each client. Player controllers on the client are not aware of other player
    controllers so we are going to do some things to help get information from other player controllers into our
    lobby menu.

Useful Nodes
^^^^^^^^^^^^

*   `Is server <https://docs.unrealengine.com/en-US/BlueprintAPI/Networking_1/IsServer/index.html>`_:
    Lets you know if you are the server or not. Useful in control flow logic.
*   `Has Authority <https://docs.unrealengine.com/en-US/BlueprintAPI/Networking_1/HasAuthority/index.html>`_ +
    Branch (Shortcut: ``Switch Has Authority``): Allows you to run code depending if you are the authority
    (server) or remote (client).
*   `Execute Console Command <https://docs.unrealengine.com/en-US/BlueprintAPI/Development/ExecuteConsoleCommand/index.html>`_:
    Useful for server travel and joining games

    *   ``servertravel``: If you are the host take the entire server with you to a map::

            servertravel /JeffSandbox/Maps/Arena_0

        ..  note::

            To when ``servertravel``, use it within the game mode (done in tutorial). Also make sure
            seamless travel is set in class defaults for the game mode.

            Also ``servertravel`` should be done in standalone mode to avoid bugs

    *   ``open``: Use to join a server by its ip address::

            open <ip_address>

*   If you are kicking someone, make sure that kick function  is running on the owning client
*   If a bug is running you ragged. it may be because a reference to self is missing somewhere.

Spawning
^^^^^^^^

*   For designated spawn points, on the player start there is a player start tag you can define. You can filter
    out based on tag an assign 2 different locations of where to spawn people.


UI
--

*   If your widget appears over other widgets you don't need a canvas panel




