# LazyNet
Chess Bot using Convolutional Neural Network
![image](https://github.com/rahulrao9/LazyNet/blob/main/board.png)

***Link to the dataset***

[dataset](https://drive.google.com/file/d/1LdWdLlfct93WfNNdiraBxJnBUqT3Oxll/view)

* Our engine, in addition to using deep learning, uses classic AI algorithms like the minimax which enables accurate decision making at each step.
* Speed is an important factor for any intelligent system. The alpha-beta pruning algorithm has been implemented to increase speed of decision making.

***Data structure***
A chess board is represented in our model as an 8 × 8 × 6 image, with two dimensions covering the chess board and six channels corresponding to each possible piece; a different representation is used for each piece since its value is of discrete worth - the difference between two pieces is not continuous and so cannot be measured on the same channel.
