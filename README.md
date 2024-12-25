**Part I: Define an RL Environment**

In this part, we will define a grid-world reinforcement learning environment as an MDP. While building an RL environment, you need to define possible states, actions, rewards and other parameters.

STEPS:

1. Choose a scenario for your grid world.
   An example of idea for RL environment:
      • Theme: Lawnmower Grid World with
        batteries as positive rewards and rocks as
        negative rewards.
      • States: {S1 = (0,0), S2 = (0,1), S3 = (0,2),
        S4 = (0,3), S5 = (1,0), S6 = (1,1), S7 =
        (1,2), S8 = (1,3), S9 = (2,0), S10 = (2,1),
        S11 = (2,2), S12 = (2,3), S13 = (3,0), S14 =
        (3,1), S15 = (3,2), S16 = (3,3)}
      • Actions: {Up, Down, Right, Left}
      • Rewards: {-5, -6, +5, +6}
      • Objective: Reach the goal state with
        maximum reward

2. Define an RL environment following the scenario that you chose.
Environment requirements:
  • Min number of states: 20
  • Min number of actions: 4
  • Min number of rewards: 4

Environment definition should follow the Gymnasium structure, which includes the basic methods. You can use RL Environment demo as a base code.

def __init__:
  # Initializes the class
  # Define action and observation space

def step:
  # Executes one timestep within the environment
  # Input to the function is an action

def reset:
  # Resets the state of the environment to an initial state
  
def render:
  # Visualizes the environment
  # Any form like vector representation or visualizing using matplotlib is sufficient
  
3. Run a random agent for at least 10 timesteps to show that the environment logic is defined correctly. Print the current state, chosen action, reward and return your grid world visualization for each step.


**Part II: Implement SARSA**

In this part, we will implement the SARSA (State-Action-Reward-State-Action) algorithm and apply it to solve the environment defined in Part I. SARSA is an on-policy reinforcement learning algorithm where the agent updates its Q-values based on the current state, action, reward, and next state-action pair. It balances exploration and exploitation to optimize learning.

STEPS:

1. Implement the SARSA algorithm to solve the environment defined in Part I.

2. Provide the evaluation results:
     • Print the initial Q-table and the trained Q-table
     • Plot the total reward per episode graph (x-axis: episode, y-axis: total reward per episode).
     • Plot the epsilon decay graph (x-axis: episode, y-axis: epsilon value)
     • Greedy policy evaluation: run your environment for at least 10 episodes,where the agent chooses only greedy actions from the learned policy. Include a plot of the total reward per episode.

3. Hyperparameter tuning. Select at least two hyperparameters for better SARSA performance. You can explore hyperparameter tuning libraries, e.g. Optuna or perform manual tuning. Parameters to tune (select 2):
    • Discount factor (γ)
    • Epsilon decay rate
    • Epsilon min/max values
    • Number of episodes
    • Max timesteps
   
Try at least 3 different values for each of the parameters that you choose.

4. Provide a short description on how these hyperparameters influence performance. Suggest the most efficient hyperparameter values for your problem setup. Combine all the parameters that return the best results, e.g. faster training, better performance and use it as the best model. Provide the evaluation results (refer to Step 2) for the setup the returns the best results.

5. Provide the evaluation results (refer to Step 2) for the setup the returns the best results.


**Part III: Implement N-step Double Q-learning**

Apply the n-step Double Q-learning algorithm to solve the environment defined in Part I.

STEPS:

1. Implement the n-step Double Q-learning algorithm to solve the environment defined in Part I. Modify your SARSA implementation to incorporate the n-step Double Q-learning update rule.

2. Experiment with hyperparameters to further optimize n-step Double Q-learning. Parameters to try include discount factor (γ), epsilon decay rate, epsilon min/max values, number of episodes, and max timesteps. Return the best model setup.

3. Provide the results with different values of n (1, 2, 3, 4, 5). Determine the optimal n-step return for your environment:
      • Print the initial and trained Q-tables for each value of n.
      • Plot the total reward per episode for each value of n.
      • Plot the epsilon decay graph for each value of n.
      • Run the environment for at least 10 episodes using only greedy actions for each value of n. Plot the total reward per episode.
   
   Provide the evaluation results and your explanation. Suggest the most efficient n value and hyperparameter setup for your problem.




