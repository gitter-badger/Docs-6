=======================
Basic Minigame Creation
=======================

Overview
========

This page details how to create a basic minigame using MinigameCore. This page assumes you have already completed :doc:`Setting up your IDE <settingup>`.

Starting Development
====================

Minigame
~~~~~~~~

The basis of a plugin using MinigameCore is the ``Minigame`` object. It provides the user access to all of the functions that MinigameCore offers. 
An example ``Minigame`` object can be seen below:

	.. code-block:: java
	
		import me.flibio.minigamecore.main.Minigame;
		import org.slf4j.Logger;
		import org.spongepowered.api.Game;

		Minigame minigame = new Minigame("My Minigame", game, logger);
		
Managers
~~~~~~~~
		
MinigameCore is based around managers. Each manager has unique capabilities that help developers make better minigames, faster. 
A full list of the managers in MinigameCore can be found below:

	=====================  =========================================================
	Manager                Description
	=====================  =========================================================
	ArenaManager           Manages all of the ``Arena`` objects in a minigame
	EconomyManager         Provides methods to interact with economy plugins
	FileManager            Provides easy-to-use file management
	KitManager             Provides minigame kit tools
	ScoreboardManager      Provides easy scoreboard creation and management
	TeamManager            Allows developers to easily create teams
	=====================  =========================================================
	
The ``ArenaManager`` is the most important manager. Learn more about arenas in the next section.

Arena
~~~~~

The ``Arena`` object allows developers to create an arena with a lobby, spawnpoints, and more. An example Arena object can 
be seen below:

	.. code-block:: java
	
		import me.flibio.minigamecore.main.Minigame;
		import me.flibio.minigamecore.arena.Arena;
		import org.slf4j.Logger;
		import org.spongepowered.api.Game;
		
		//Create the new Minigame
		Minigame minigame = new Minigame("My Minigame", game, logger);
		//Create the new Arena
		Arena arena = new Arena("Arena Name", game, this);
		//Add the arena to the ArenaManager
		minigame.getArenaManager().addArena(arena);

Learn more about the Arena object :doc:`here <arenacustomization/index>`.