Mind_Masterr

A fast, simple, scriptable implementation of Mind_Masterr in Python , with an AI solver.

How do I install ?

Make sure you have python 3.6+ on your machine, with the pygame and numpy libraries installed.

This code is portable, so all you have to do is clone the repository and extract the files.

Playing the game

To play the game yourself, run Mind_Masterr.pyw. The grid size and number of mines can be changed in the file settings.json.

 
<img width="321" alt="Capture1" src="https://github.com/user-attachments/assets/801746c2-ed1f-4dd2-83d2-f92fa00beb22">

























The solver algorithm
To run the solver, run Mind_Masterr_ai.py. The grid size and number of mines, as well as other parameters, can be changed in the code at the bottom

of this file. By default, 10 games are solved, then the solver stops and prints the number of wins and losses. This is very satisfying :)

Keyboard controls:

SPACE: pauses and unpauses the solver

. (PERIOD key): advances the solver one step at a time, when it is paused

As opposed to starting at the corners (eg https://dash.harvard.edu/bitstream/handle/1/14398552/BECERRA-SENIORTHESIS-2015.pdf), this solver starts by guessing a square at random.


The game position is analysed using some hardcoded rules, which will find all the squares which are definitely mined or safe (except in rare cases, when there is a safe square that the ruleset misses). If there are no such squares found, the algorithm tries to find a square with a low probability of being mined, and guesses. A full depth-first search would find the exact probabilities, at the expense of involving some very large integers and potentially being slow. I'm planning to maybe implement one at some point.

The solver (contained in the BasicRulesetAI class) has been written to be subclassable, so that better algorithms could be implemented and compared.


 

