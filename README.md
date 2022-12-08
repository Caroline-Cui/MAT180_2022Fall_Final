# MAT180_2022Fall_Final
# Learning to Play Pong

<!-- ABOUT THE PROJECT -->
## Objective
In this project, we will be training a model to learn to play Pong without human knowledge of the game. We will be using the OpenAI gym to run and interact with the Pong Atari game and the deep Q-learning algorithm. 

## Overview
As pre-trained model is provided, we will make modifications to improve its ability to learn and train the provided pre-trained model to acceptable performance. The model will use its Q network to decide what moves to take when playing the game. This network will push each decision it made to an experience buffer. This replay buffer will be polled from to make updates to the Q network using the loss function. The network is contained within dqn.py. We will train our network using run_dqn_pong.py. The environment will keep playing games of pong until either player gets 21 points.

## Learning to Play Pong
To help combat the difficulty in training time, we used a provided network that is partially trained. Moreover, to prevent code from crashing or server from getting shut off, we used torch.save to save our model occasionally when training neural networds.

We also used run_dqn_pong.py currently to record the loss and rewards in losses and all rewards respectively. We continued to train the model by running run_dqn_pong.py. To achieve good performance, we trained the model for approximately 500,000 more frames. We want to optimize different values for hyper-parameters such as γ and the size of the replay buffer.

When we tried training our model the first few times, we noticed that it would start around -20 average reward, go up to around -18, then go back down to -20 after around 120k frames. At this point, we would Ctrl-C and try making changes since we assumed it wasn’t working. One of the best changes we made to prevent it from going back down in reward averages was changing the way that we saved the model. Instead of simply saving it every 5k frames as we did at first, we modified it so that it would save the maximum average reward for the last 10k frames (the same value it prints in the console). Whenever a new maximum average was reached, the model would be saved. After 1 million frames, this achieved an average reward of 19.5. When running test_dqn_pong.py it won every game except for one game. However, after running another training session on that same model, we found the rewards incresaed much faster than the first one.

## Group Member

Ye Cui - cycui@ucdavis.edu

Yuxin Chen - vyxchen@ucdavis.edu

Yizhang Huang - 



