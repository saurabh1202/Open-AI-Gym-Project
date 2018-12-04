# Open-AI-Gym-Project

Q1) Mountain Car Policy using No learning:





Q2) CartPole Policy using No Learning:

The basic task in the CartPole problem lies in balancing the pole on the cart while moving the cart in either left or right direction. There are bounds to CartPole disobeying which the episode terminates. The observation space of the CartPole environment returns 4 variables. State, reward, done and info. State has 4 features. The 3rd index of State gives the angle of the CartPole. The policy that I applied moves the cart in the direction in which the pole is leaning. Suppose the pole has a negative angle which means its inclined towards the left hence the policy moves the cart towards left and vice-versa. This is done in hope of bringing the pole to an upright position by shifting its center of gravity. This policy does not last the 200 steps for the problem to be successful. But it performs better than random action search on average. 
I did 100 episodes of 200 steps each. This was the performance of the policy over 100 episodes.

Average reward over 100 episodes = 41.3
Max reward in an episode over 100 episodes = 64.0
Min reward in an episode over 100 episodes = 24.0

Q3) Mountain Car using Cross-Entropy method

Inspired by the Cross-Entropy method taught in class (Github repo schneider128k). First, we initialize the hyperparameters according to the mountain car environment. Since the state space is a vector of 
[position, velocity], we set the state size to 2. The MountainCar-v0 has a discrete action space which is a vector of [0,1,2] where 0 represents push left, 1 represents No push and 2 represents push right. Hence, we set the size of the action size to 3. Maximum episodes are set to 100 and maximum steps are set to 200 since it is one of the terminal states for an episode. We set the input layer as the states [position, velocity] and feed them to a fully connected layer of size 128. This layer is then fed to another fully connected layer of size of the action space. We apply softmax regression on this logits to get the action probabilities. We get one hot action vector using tf.one_hot()after which we apply tf.nn.softmax_cross_entropy_with_logits_v2()on the logits to get the cross_entropy. We use reduce_mean() on this to get cost on which we use AdamOptimizer and minimize the cost. After training this network and testing it did not converge with the total reward being -200.
Total reward: -200.0
Total reward: -200.0
Total reward: -200.0
Total reward: -200.0
Total reward: -200.0
Total reward: -200.0


Q4) Algorithm methods Overview

DFS: Algorithm used to traverse graph or tree structures. Starts from a root node and goes to the depth of branch. Used in maze solving.

BFS: Used to traverse graph or trees structures. Starts from a root node and explores all the neighboring nodes at the same depth. Also used in maze solving

Uniform Cost Search: UCS is algorithm used to search in branches with almost the similar costs. UCS is used to find the shortest path or the optimal cost in a weighted graph.

Heuristic: Heuristic is a method that is employed for discovery. Its not an optimal or perfect method but reaches the immediate goal. Heuristic is used in trees to find optimal path.


Adversarial search: Adversarial search is a minimax search used to find the best moves in a game. It uses tree data structure and captures all the moves a player can make where each move is represented as a loss or gain for one of the players.

Expectimax: Similar to Adversarial search this is used in two player zero sum gains where one’s loss is other’s gain. But, here there is an additional factor of chance. This has a chance node which takes the 
expected value of a random event occurring.

Reinforcement Learning: Uses the action and state space of the environment. It is a type of machine learning algorithm which learns from trial and error using output from its own actions and experiences. Used in games to check and learn from the outcome that the player makes.

Q-Learning: It is a Reinforcement learning technique. It is used to learn a policy that maximizes the total reward over all successive steps thus telling the agent what action to take. It forms an equation of a combination of old value and the estimate of optimal future value.

Deep Learning: Deep learning are neural network algorithms modeled after human brain to find patterns. They are used for classification or regression problems. Learning can be supervised, unsupervised or semi-supervised. Used in areas like computer vision, NLP etc.

Cross Entropy method: Cross Entropy method used for rare-event probability estimation in discrete event simulation systems and for optimization. The cross-entropy procedure involves generating a random data sample according to a specified mechanism and updating the mechanism based on the data to produce better samples in next iteration.





