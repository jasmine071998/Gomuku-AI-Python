# Gomuku-AI-Python

Built an efficient AI system that plays the Gomuku game.

**Code Structure**

When you are building your custom AI to play the Gomuku game, ensure that you make the changes in submission.py only and not in any other file as the other files contain the implementation of the baseline minimax(i.e your opponent in the game)

• gomoku.py: This module contains the implementation of the Gomoku game, including methods to
list valid actions for every state, perform an action in a given state, and calculate the score in a game state.
• compete.py: This module runs a full game between two players. Each player can be controlled by a human or various automated policies.
• performance.py: This module runs several games between your AI and the baseline policy. The
plots at the end visualize the final scores and run times of each AI. It saves the results in a file named perf.pkl.
• policies/: The modules in this sub-directory include various policies that can be selected for each
player.
o human.py: This policy is human-controlled
o random.py: This policy chooses actions uniformly at random
o minimax.py: This policy chooses actions using an augmented Minimax Search
o submission.py: This policy will use your AI implementation

**How to play**

You can run a game between two policies by running compete.py on the command line with options to specify board size, win size, and each player’s policy. For example, the command
python compete.py -b 15 -w 5 -x Human -o Minimax
will run a game on a 15x15 board with 5 in a row to win, where you control the max player, and the min player selects actions randomly. For each policy you must write the exact name of the policy class (casesensitive). The available policies are Human, Random, Minimax, and Submission (which is yours). Press Ctrl-C, or a similar command in your operating system, to interrupt the script at any time and terminate early before the game is over.
Run the script performance.py to play your AI against the Minimax baseline. The baseline is the max player and gets to go first. Your AI is the min player and goes second. This means that your AI wins when the final score is negative. Multiple games are played, and the final game scores and run times of each game are recorded. 

**Our implementation**

**Novelty**

The Gomoku AI stands for a significant advancement planning mechanism. It has several new features that improve its ability to make decisions. The following are the implementation's key components:
● Custom evaluation functions: AI uses custom evaluation functions that go beyond the basic heuristics. Our implementation considers known patterns and their design values to examine both individual positions and board maps. It includes a sophisticated scoring system based on the potential of the sites against the number of open ends, and the length of stone lines, making it a clever projection point.
● Pattern recognition: Throughout the whole gameplay session, this AI can identify new patterns—a characteristic that is uncommon in the regular Minimax algorithm or simple MCTS implementation.
● Dynamic learning: The ‘learn_new_pattern’ approach demonstrates a new approach by dynamically updating the AI's existing knowledge during game play, allowing it to adapt to the opponent's strategies.
● Enhanced move ordering: The ‘get_prioritized_moves’ method introduces a sophisticated approach to the move selection. It focuses on central control and proximity to existing rocks. This is an algorithmic enhancement that improves the move selection process, and the final product.

**Method**

In this project on developing a sophisticated strategy for Gomoku, we adopted a multifaceted approach that hinges on the interplay of pattern recognition, dynamic board analysis, and strategic move selection. This strategy emphasizes the importance of understanding and creating patterns on the board that have an advantage while staying vigilant against the opponent’s
tactics.
Our strategy revolves around the concept of pattern recognition and analysis. We meticulously define and recognize specific sequences of stone placements, each is then characterized by its coordinates and the player’s identifier. The strategic value of these patterns is crucial for this code. We assess this by considering the number of stones and their potential to contribute towards a win. We quantified the value of these patterns using the formula V(p) = k * length(p), where ‘length(p)’ indicates the number of stones in a pattern, and ‘k’ represents a constant that assigns a base value to each stone within a pattern.
Another key part to our strategy is board analysis that is dynamic. We scrutinized each turn of the board with respect to the fixed size of the board and fixed length of winning pattern, considering recent moves and the state of the game in progress. This ongoing analysis allows us to evaluate patterns for their win potential as well as give them numerical values to guide our strategic decision-making.
The last pillar in our approach involves the selection of a good move for any given situation. We then made a ranked list of possible moves based on their strategic importance. This evaluation process took into account such elements as central positioning on the grid and proximity to existing stones. With this method, we ensure that every move is not only responsive to an opponent’s play but also rational given current position on the board, strategic significance of stone lines (including length and open ends) and chances for winning or defense.
The way this is presented with precision has changed the Gomoku game. It’s not just about
keeping the opponent in check; it involves strategic planning and control of the board as well as moves which serve dual purposes in attack and defense. The game's strategic depth adds an extra layer of complexity, turning it into a clash of patterns and anticipations rather than just moves.

**Results**

The Gomoku AI gives an impressive performance with an average final score of -200. Integrating custom algorithms, pattern recognition, dynamic board evaluation, and pre-emptive threat management represents adaptability and depth. The AI’s ability to learn strategies in real-time, along with a good approach to evaluate game states makes it a highly challenging and competent opponent.
However, implementing deep learning techniques could enhance AI’s pattern recognition capabilities by learning complex strategies. Exploring other tree search algorithms with advanced exploration-exploitation balancing could offer more better ways to handle complexity.

 ![image](https://github.com/jasmine071998/Gomuku-AI-Python/assets/43840262/7962b8bd-c67e-41bf-a03f-4b4ab9feef2c)
