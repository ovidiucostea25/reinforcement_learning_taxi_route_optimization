# reinforcement_learning_taxi_route_optimization
 Train a reinforcement learning (RL) agent to solve the Taxi-v3 Gymnasium environment, ensuring optimal AI-driven transportation


In the quest for efficiency and effectiveness in urban transportation, finding the optimal routes to take passengers from their initial locations to their desired destinations is paramount. This challenge is not just about reducing travel time; it's about enhancing the overall experience for both drivers and passengers, ensuring safety, and minimizing environmental impact.

You have been asked to revolutionize the way taxis navigate the urban landscape, ensuring passengers reach their destinations swiftly, safely, and satisfactorily. As an initial step, your goal is to build a reinforcement learning agent that solves this problem within a simulated environment.

The Taxi-v3 environment
The Taxi-v3 environment is a strategic simulation, offering a grid-based arena where a taxi navigates to address daily challenges akin to those faced by a taxi driver. This environment is defined by a 5x5 grid where the taxi's mission involves picking up a passenger from one of four specific locations (marked as Red, Green, Yellow, and Blue) and dropping them off at another designated spot. The goal is to accomplish this with minimal time on the road to maximize rewards, emphasizing the need for route optimization and efficient decision-making for passenger pickup and dropoff.

Key Components:
Action Space: Comprises six actions where 0 moves the taxi south, 1 north, 2 east, 3 west, 4 picks up a passenger, and 5 drops off a passenger.
Observation Space: Comprises 500 discrete states, accounting for 25 taxi positions, 5 potential passenger locations, and 4 destinations.
Rewards System: Includes a penalty of -1 for each step taken without other rewards, +20 for successful passenger delivery, and -10 for illegal pickup or dropoff actions. Actions resulting in no operation, like hitting a wall, also incur a time step penalty.


Project steps:
- Train an agent over 2,000 episodes, allowing for a maximum of 100 actions per episode (max_actions), utilizing Q-learning. Record the total rewards achieved in each episode and save these in a list named episode_returns.
- What are the learned Q-values? Save these in a numpy array named q_table.
- What is the learned policy? Save it in a dictionary named policy.
- Test the agent's learned policy for one episode, starting with a seed of 42. Save the encountered states from env.render() as frames in a list named frames, and the sum of collected rewards in a variable named episode_total_reward. Make sure your agent does not execute more than 16 actions to solve the episode. If your learning process is efficient, the episode_total_reward should be at least 4.
- Execute the last provided cell to visualize your agent's performance in navigating the environment effectively. Please note that it might take up to one minute to render.
