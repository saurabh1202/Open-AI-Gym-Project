# Open-AI-Gym-Project

Q1) Mountain Car Policy using No learning:





Q2) CartPole Policy using No Learning:

The basic task in the CartPole problem lies in balancing the pole on the cart while moving the cart in either left or right direction. There are bounds to CartPole disobeying which the episode terminates. The observation space of the CartPole environment returns 4 variables. State, reward, done and info. State has 4 features. The 3rd index of State gives the angle of the CartPole. The policy that I applied moves the cart in the direction in which the pole is leaning. Suppose the pole has a negative angle which means its inclined towards the left hence the policy moves the cart towards left and vice-versa. This is done in hope of bringing the pole to an upright position by shifting its center of gravity. This policy does not last the 200 steps for the problem to be successful





Algorithm methods Overview
