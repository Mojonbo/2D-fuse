Matthew Hirano
14/16/2016
Final Project- "Keep Talking and Nobody Explodes" bomb defusal simulator

--- Run Information ---

Important; this game was made to run on python 32 bit 3.5.2 with the corresponding version of Pygame. I don't know if alternate versions of Pygame will work with it. Additionally, whenever a new sprite is loaded, the console gives a 'Libpng warning.' This will pile up over the course of a game, but it's not very important- it just means that pygame doesn't like something about the RGB values in the images, but it successfully loads them anyways. I don't want to reduce image quality by manually 'crushing' the values (and transparency) of each image.

Additionally, please download the Bombimgs file to the directory; it contains all the sprites that the game calls.After that, you just need to run the python file to start the game!

--- What is this? ---

bomb.py is a game that uses the module Pygame to create a bomb-defusing simulator. It presents a bomb to the player with a randomized number of three types of modules- a typical Hollywood "cut the red wire, or black wire?" kind of defusal situation. Using an online guide (http://www.bombmanual.com/manual/1/html/index.html), another person who cannot look at the screen instructs the player how to defuse the bomb- but cutting wires, pressing and holding buttons, or pressing buttons in correct orders. Hints to what to do are placed on the bomb in the form of visuals- batteries, a serial tag, etc.
This program is based on a purchasable VR game called "Keep Talking and Nobody Explodes," which I just enjoyed enough to make a 2D version of.

--- Programming notes ---

In terms of programming, there are a few steps; I used classes to define each interactive puzzle within the game, that could be called upon to return its status (what color it is, whether it's been pressed or not, or whether it's been solved, for example.) I also wrote some functions to construct these puzzles randomly at the start of the game. 

The bulk of the game runs in the gameloop, which is a common tool in game design. In a continuous loop, the game counts how much time has passed, updates the clock, then thanks to pygame, will take a queue of commands (such as clicking or releasing the mouse). Pygame can also detect where these mouseclicks occur, letting the player interact with each module.

I used classes to construct many decoartive objects, too- lights that change color, or a timer that counts down each second. Almost every object in this game uses image sprites; Pygame lets me import an image, and then the code determines where to draw the images to update appearances. Drawing a new image over an old one lets me change light colors, make a button change appearance as it's pressed, or even for just erasing the clockface to draw a more recent time on it every frame.

--- Bugs and improvements ---

Currently, the program seems to work fine- puzzles are solved only according to rules from the game manual, and there's no way to crash the game. I encountered many many bugs along the way that would allow the player to get around these rules (eg, clicking down on a button, moving the mouse off of the button, then releasing the mouse counted as a click, but not a release), but I've been pretty thorough in removing any such bugs. Finally, a constructor randomizes the puzzles/decor on the bomb every game- by running it repeatedly, I don't think that there is any combination that the contrustor can create that results in a crash.

The actual game contains far many more puzzles than the three I have here, but I promised in the design document the wire/button/keypad puzzles. I may take this project beyond the semester and add more, given time.


References: Most understanding for using Pygame functions comes from the following websites and their examples:
http://thepythongamebook.com/en:pygame:start
http://www.pygame.org/docs/

Although I frequently copied function commands from here, like how to load a sprite, or detect mouse collision, each individual class and function is my own creation based on these directions.

Game inspiration, manual, and Greek/Cyrillic image assets are from http://www.bombmanual.com/

LCDAT&T font is open source from DAfont.com

All other images and code are original by Matthew Hirano