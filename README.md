# MAT180_2022Fall_Final
# Learning to Play Pong

<!-- ABOUT THE PROJECT -->
## Objective
In this project, we will be training a model to learn to play Pong without human knowledge of the game. We will be using the OpenAI gym to run and interact with the Pong Atari game and the deep Q-learning algorithm. 

## Procedure
We will first build a pre-trained model. Then we will make modifications to improve its ability to learn and train the provided pre-trained model to acceptable performance.
The model will use its Q network to decide what moves to take when playing the game. This network will instead push each decision it made to an experience buffer. This replay buffer will be polled from to make updates to the Q network using the loss function. The environment will keep playing games of pong until either player gets 21 points.

## Contact

Ye Cui - cycui@ucdavis.edu

Yuxin Chen - vyxchen@ucdavis.edu

Yizhang Huang - 



