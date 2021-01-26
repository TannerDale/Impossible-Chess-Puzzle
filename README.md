The Impossible Chessboard Puzzle is a math puzzle involving two prisoners, a sadistic captor, a chessboard, and some coins.

The Puzzle:
You and your friend have been captured. Your sadistic captor gives you a challenge and tells you he'll let you both go if you can solve it.
Your challenge is this: a coin is randomly laid on every space of a chess board. Some are heads, some are tails (or all heads and all tails, who knows).
Your key to freedom is placed underneath a random coin. Your captor explains you must flip one, and only one, coin to tell your friend which coin the key is under.
You cannot talk to your friend after flipping the coin, and your friend will not have seen the board before walking in to solve the puzzle.
How do you do it?

The Solution:
Set-up:
  Assign each tile a 6-bit binary ID starting with 000000 in top-left corner, ending in 111111 bottom-right.
  Split board into six groups. Group 1 is defined by all tiles (cells) with a 1 as the first digit (000001, 000011, 000101, 000111, etc) Group 2 is all tiles with a 1 in the 2nd   digit, and so on.
  
Person 1:
  If sum of all heads in each group is even, it decodes to 1, if odd, it decodes to 0. Group 1 is the first digit and group 6 is the last digit of a 6-bit binary number representing the decoded board.
  Compare the binary location ID of the tile the key is in with the decoded board state. For each digit, if the digits match, record 0 in new 6-bit number, if not, record 1.
  The new number represents the tile whose coin you flip, thus encoding the board to read the same 6-bit number as the location ID of the coin.
  
Person 2:
  Decode board through same process as Person 1. The result is the binary ID of the tile with the key in it.

The Code:
Prompts for key placement.
Creates or imports an excel sheet (using openpyxl) to store binary IDs for chess tiles (cells). Decodes the current state of the chess board to a 6-bit binary number.
Flips one 'coin' to recode board to binary ID of key location.
Decodes newly created board to get key location.
Prints the key location and related decoding data.

