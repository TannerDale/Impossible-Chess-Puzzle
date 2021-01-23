# impossible_chess_v2.py
The Puzzle:
You and your friend have been captured. Your sadistic captor gives you a challenge and tells you he'll let you both go if you can solve it.
Your challenge is this: a coin is randomly laid on every space of a chess board. Some are heads, some are tails (or all heads and all tails, who knows).
Your key to freedom is placed underneath a random coin. Your captor explains you must flip one, and only one, coin to tell your friend which coin the key is under.
You cannot talk to your friend after flipping the coin, and your friend will not have seen the board before walking in to solve the puzzle.
How do you do it?

The Code:
Prompts for key placement.
Creates or imports an excel sheet (using openpyxl) to store binary IDs for chees tiles (cells). Decodes the current state of the chess board to a 6-bit binary number.
Flips one 'coin' to recode board to binary ID of key location.
Prints the key location and related decoding data.

Modify working directory in line 8.
