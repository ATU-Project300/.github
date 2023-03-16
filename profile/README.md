# Odyssey

Repos for Odyssey, our Project 300 in ATU.

## Goal

To create a Windows application and website to help users pick the best emulator to play their game of choice.

## The issue aim to solve

Console emulators are always changing. With each update, more games become playable and sometimes issues can arise. Due to this inconsistency, stating that "X emulator is best for playing Y game", may not hold true for very long.

This is particularly true with 6th and 7th generation consoles, when many games were released on as many platforms as possible. This has now resulted in users being left to research the compatibility of the game they wish to play, obtaining a copy of the game for the platform and then installing the emulator that works best for that game.

There are many examples of this such as Red Dead Redemption for the PlayStation 3 and Xbox 360. RPCS3 and Xenia are the emulators used for these consoles, both of which are updated very frequently. As mentioned previously, each update can change the state a given game is in, so it's not easy to declare one emulator better than the other for this particular game.

There may also be issues with a user just not knowing which emulator to use for a particular game, regardless of how many emulators there are or other variables.

## General overview

The Odyssey website provides the ability for users to add games to the database and to rate their experience with existing games. The website can also be used as a general reference for which emulator to use for a given game. Any operations which would modify the database contents, such as rating a game, require the user to be logged in with OAuth.

The Odyssey desktop application allows for users to play the rated games as in the database. It is designed such that the user need only provide the game files (ROMs/ISOs we cannot legally distribute), while the application provides the emulators and information about the games.

Combining these two systems, users can play their favourite games with minimal barriers between them and their games. It also allows more technical users to contribute to the application by creating an account or logging in with Google and adding their games and rating their experience emulating those games.

At the time of writing, the Odyssey website functions as follows:

* Games and Emulators are stored in a NoSQL database.

* The database is accessible via our API.

* The Angular website displays games data via the API.

* Logged in users can rate their experience emulating a game.

* This rating influences the average rating, which is displayed on the site.

... and the WPF desktop app functions as follows:

* Game and Emulator data is read from the API.

* Games data can be viewed in more detail upon clicking a game cover.

* From clicking a game cover, a game can be ran, where its emulator and game files are detected automatically.

* Emulator data is used to allow for downloading emulators from the Emulator section of the app.