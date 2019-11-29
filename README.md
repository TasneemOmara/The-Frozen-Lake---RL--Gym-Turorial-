# The-Frozen-Lake-QLearning

## This Repository is based on:  
1- OpenAI gym: https://gym.openai.com/envs/FrozenLake-v0/  
2- Tutorial by Mohamed ElSayed

## The Frozen Lake Environment
Winter is here. You and your friends were tossing around a frisbee at the park when you made a wild throw that left the   
frisbee out in the middle of the lake. The water is mostly frozen, but there are a few holes where the ice has melted.   
If you step into one of those holes, you'll fall into the freezing water. At this time, there's an international frisbee     shortage, so it's absolutely imperative that you navigate across the lake and retrieve the disc. However, the ice is   
slippery, so you won't always move in the direction you intend.       


## FrozenLake-v0
The agent controls the movement of a character in a grid world. Some tiles of the grid are walkable,   
and others lead to the agent falling into the water. Additionally, the movement direction of the agent  
is uncertain and only partially depends on the chosen direction. The agent is rewarded for finding   
a walkable path to a goal tile.

![Image of Frozen-Lake](https://analyticsindiamag.com/wp-content/uploads/2018/03/Frozen-Lake.png)


## Q-learning 
![Image of Q-learning code](https://developer.ibm.com/developer/articles/cc-reinforcement-learning-train-software-agent/images/fig03.png)

### The algorithm 
1- Initialize the decaying epsilon (i.e we will divide num of episodes passed) with 1    
2- Initialize the Q-table, the rows equal the number of the states while the columns equal the number of actions  
3- Get a random number, if it's smaller than epsilon, the agent will do exploration, else, it will do exploitation. Exploration gets a random action given a state represented by a certain row, exploitation gets the maximum action given that row    
4- Get the next-state, the reward, and if the episode is finished after performing the calculated action  
5- Save the old value given the past state and the action  
6- Get the maximum Q-value in the next-state   
7- Update the new value using the Q-learning equation  
8- Update the old value with the new value in the Q-table   
9- Update epsilon, and exit the loop when the episode is finished   
