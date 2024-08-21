# Taxi-v3-Reinforcement-Learning-Project


Taxi-v3 Reinforcement Learning Project
This project aims to develop a reinforcement learning agent using Q-learning to solve the Taxi-v3 environment, a classic problem provided by the gymnasium library. The environment simulates a taxi that needs to pick up a passenger at a specific location and drop them off at their destination with optimal efficiency.

Project Overview
Environment Description
Environment: Taxi-v3 (5x5 grid)
Action Space: 6 discrete actions
0: Move south
1: Move north
2: Move east
3: Move west
4: Pickup passenger
5: Drop off passenger
Observation Space: 500 discrete states
25 taxi positions
5 possible passenger locations
4 destination locations
Rewards and Penalties
+20 for successful passenger drop-off.
-10 for illegal pickup or drop-off actions.
-1 for each time step to encourage efficiency.
Objective
The objective is to train an agent that can navigate the taxi grid, efficiently pick up passengers, and drop them off at the correct locations with minimal steps and penalties.

Implementation
Dependencies
Ensure you have the necessary libraries installed:

bash
Copy code
pip install gymnasium imageio
Training the Agent
We trained the agent over 2,000 episodes using Q-learning with a maximum of 100 actions per episode. The Q-values were updated using the following parameters:

Learning Rate (α): 0.1
Discount Factor (γ): 0.9
Exploration Rate (ε): 0.1 (decayed over time)
Q-values and Policy
The Q-values were learned and stored in a q_table (numpy array). The optimal policy was derived from these Q-values, mapping each state to the best action.

Testing the Agent
We tested the agent's learned policy over a single episode, starting with a seed of 42. The agent was allowed a maximum of 16 actions to solve the episode. The test results were captured and saved as a GIF, showcasing the agent's behavior in the environment.

GIF Visualization
The agent's performance can be visualized through the generated GIF taxi_agent_behavior.gif, which captures the agent's steps during the episode.

Files Included
taxi_agent_behavior.gif: Visual representation of the agent's behavior.
main.py: Script to train and test the agent.
README.md: This document, explaining the project.
How to Run
Clone the repository:

bash
Copy code
git clone https://github.com/your-repo/taxi-rl-agent.git
cd taxi-rl-agent
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Run the training and testing script:

bash
Copy code
python main.py
The GIF of the agent's behavior will be saved in the root directory.

Conclusion
This project demonstrates the use of Q-learning in a simulated environment to optimize a taxi's operations within a grid world. The approach could be further extended and adapted to more complex, real-world scenarios.
