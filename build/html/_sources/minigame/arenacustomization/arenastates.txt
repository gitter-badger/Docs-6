Arena States
============

This page describes the ``ArenaState`` in detail and how to customize it.

What is an ArenaState?
----------------------

An ``ArenaState`` is used to tell what the arena is currently doing. There are currently 6 default ``ArenaStates``:

	**LOBBY_WAITING**
		The arena is in the lobby, and waiting for the minimum players to join.
	**LOBBY_COUNTDOWN**
		The arena is in the lobby, and the minimum players have been reached. The arena is now counting down for a set amount of time.
	**COUNTDOWN_CANCELLED**
		The arena is in the lobby, and had dipped below the minimum players. This is only activated for a few milliseconds, and will change directly back to ``LOBBY_WAITING``.
	**GAME_COUNTDOWN**
		The game is in countdown phase.
	**GAME_PLAYING**
		The game is in progress.
	**GAME_OVER**
		The game has ended and will wait 5 seconds before teleporting players back to the lobby spawn location.
	
	.. note::
		
		The behavior described is the default behavior of MinigameCore. It can be customized or disabled at the developers will.

Adding a Custom ArenaState
--------------------------

To add a custom ``ArenaState``, you will need to use the ``ArenaStateBuilder``. You need to register it with the 
``Arena`` in order for the ``Arena`` to recognize it. An example of how to do this can be found below:

	.. code-block:: java
	
		import me.flibio.minigamecore.arena.Arena;
		import me.flibio.minigamecore.arena.ArenaState;
		import me.flibio.minigamecore.arena.ArenaStateBuilder;
		
		ArenaState arenaState = ArenaStateBuilder.createBasicArenaState("Custom ArenaState");
		arena.addArenaState(arenaState); // <--- This method will return a boolean based on if it was successful or not
		
	.. note::
	
		It is possible to create an ``ArenaState`` by extending the ``ArenaState`` class, but this should only attempted by advanced users. There is little to 
		no benefit of creating an ``ArenaState`` without using the ``ArenaStateBuilder``.