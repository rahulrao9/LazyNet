# LazyNet
![image](https://github.com/rahulrao9/LazyNet/blob/main/board.png)

***Link to the dataset***

[dataset](https://drive.google.com/file/d/1LdWdLlfct93WfNNdiraBxJnBUqT3Oxll/view)

***Overview***

Create an AI that uses board evaluations to play the best move in
a given position
* Train a Convolutional Neural Network using board evaluations from the established chess engine Stockfish
* Fit 150000 boards as a 14x8x8 object to a score
* Use it to play against Stockfish
* Our engine, in addition to using deep learning, uses classic AI algorithms like the minimax which enables accurate decision making at each step.
* Speed is an important factor for any intelligent system. The alpha-beta pruning algorithm has been implemented to increase speed of decision making. Alpha-beta pruning is a way to limit computation time. White will never choose a move that gives black a better evaluation than a previously calculated move, so the rest of the right side branches are snipped after the ≤ −4 is calculated. White will always choose left branch. On the left side, we know to cut the rest of the ≥ 5 node as black would never choose a move that gives white a larger evaluation than the 3 previously calculated. Black will always choose the left branch.

***StockFish**
* Stockfish is an open-source chess engine released in 2008
* Uses raw material (piece) advantages in early, mid, and lategame to evaluate position
* Optimal piece placement for knights, bishops, and kings, pawn formation matters.
* All weighted differently over years of fine-tuning
* Finds best move through 30+ deep tree and applies evaluations for each board state.
* Ranked consistently 1st/2nd for best chess engine since 2013, only recently losing to Alphazero by the company DeepMind which uses self-play to train neural networks
* We use this engine to evaluate self created random boards and train the CNN

***Data structure***

A chess board is represented in our model as an 8 × 8 × 6 image, with two dimensions covering the chess board and six channels corresponding to each possible piece; a different representation is used for each piece since its value is of discrete worth - the difference between two pieces is not continuous and so cannot be measured on the same channel.
