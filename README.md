Select a game mode when prompted:
 for Human (X) vs Minimax AI (O)
 for Human (X) vs Alpha-Beta AI (O)
 for Minimax AI (X) vs Alpha-Beta AI (O)

Game Instructions:
The board is represented as positions 0-8:
| 0 | 1 | 2 |
| 3 | 4 | 5 |
| 6 | 7 | 8 |
Players take turns entering numbers 0-8 to place their mark
The first to get 3 in a row (horizontally, vertically, or diagonally) wins
If all squares are filled with no winner, the game is a draw

Algorithm Explanation:
Minimax Algorithm:
Recursively explores all possible game states
Assumes opponent plays optimally (minimizing your advantage)
Returns the move with the highest score for the AI player
Time complexity: O(b^d) where b is branching factor, d is depth

Alpha-Beta Pruning:
Optimized version of Minimax
Prunes branches that cannot affect the final decision

Maintains two values:
α: Best already explored option for maximizer
β: Best already explored option for minimizer

Time complexity: O(b^(d/2)) in best case (much more efficient)

Performance Comparison:
When running AI vs AI mode (option 3), the program outputs the number of nodes visited by each algorithm. Typically:
Minimax will visit hundreds of thousands of nodes
Alpha-Beta will visit significantly fewer nodes (often 10-100x fewer)
This demonstrates the efficiency gain from pruning unnecessary branches.

Customization Options:
You can modify the code to:
Change which player goes first
Adjust the delay between AI moves (change time.sleep value)
Add different difficulty levels by limiting search depth
Implement a graphical interface instead of text-based
