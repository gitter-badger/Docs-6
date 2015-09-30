===================
Setting Up your IDE
===================

Overview
========

This page will detail how to setup your IDE for MinigameCore development.

Adding Dependencies
===================

To start developing with MinigameCore, you will need to add MinigameCore as a Maven/Gradle dependency.

.. attention::

	While it is possible to add MinigameCore as a dependency without using Maven or Gradle, this is **not** recommended.

MinigameCore uses `JitPack <https://jitpack.io/>`_ to provide Maven/Gradle capabilities.

Maven
~~~~~

#. In your ``pom.xml`` file, add the JitPack repository inside of the ``repositories`` tags.

	.. code-block:: xml

		<repository>
			<id>jitpack.io</id>
			<url>https://jitpack.io</url>
		</repository>
	
#. Add the MinigameCore dependency to your ``pom.xml`` file inside of the ``dependencies`` tags. The ``-SNAPSHOT`` version will get the latest version of MinigameCore.

	.. code-block:: xml

		<dependency>
			<groupId>com.github.Flibio</groupId>
			<artifactId>MinigameCore</artifactId>
			<version>-SNAPSHOT</version>
		</dependency>
		
	.. note::

		You can swap out the ``-SNAPSHOT`` version for either a commit id (i.e. ``43e1c6447e``) or a release version (Currently not available)
		
#. Refresh your Maven dependencies.

**You should now be ready to develop plugins with MinigameCore!**

-----
		
Gradle
~~~~~~

#. In your ``build.gradle`` file, add the JitPack repository inside of the ``repositories`` block.

	.. code-block:: groovy
	
		repositories {
			maven { url "https://jitpack.io" }
		}
		
#. Add the MinigameCore dependency to your ``build.gradle`` file inside of the ``dependencies`` block. The ``-SNAPSHOT`` version will get the latest version of MinigameCore.

	.. code-block:: groovy
	
		dependencies {
			compile 'com.github.Flibio:MinigameCore:-SNAPSHOT'
		}
		
	.. note::

		You can swap out the ``-SNAPSHOT`` version for either a commit id (i.e. ``43e1c6447e``) or a release version (Currently not available)
		
#. Refresh your Gradle dependencies.

**You should now be ready to develop plugins with MinigameCore!**