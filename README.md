# moon_landing_gym

this project trains the agent to land a lunar module autonomously suing reinforcement learning. the agent learns in a simulated 2d landing environment using the gymnasium api. the goal is to land the module smoothly on a designated landing pad while minimizing fuel consumption and avoiding crashes. 

# key Features
	•	uses deep q-networks for learning
	•	provides real-time rendering of landings
	•	saves & loads trained models for evaluation
	•	generates video recordings of landings at the end


# state Space
state consists of 8 continuous values:
	1.	x (horizontal position)
	2.	y (vertical position)
	3.	vx (horizontal velocity)
	4.	vy (vertical velocity)
	5.	theta (angle)
	6.	vtheta (angular velocity)
	7.	leg1_touch (1 if left leg touches the ground, else 0)
	8.	leg2_touch (1 if right leg touches the ground, else 0)

# action Space

the agent controls the lunar lander using discrete actions:
	•	0: do nothing
	•	1: fire left thruster
	•	2: fire main thruster
	•	3: fire right thruster

# common problems (macOS)
  • ModuleNotFoundError: No module named 'gymnasium'
    solution: run pip install gymnasium[box2d]
  • ModuleNotFoundError: No module named 'imageio'
    solution: run pip install imageio[ffmpeg]
  • agent crashes constantly
    solution: increase training timesteps
  • agent doesn’t land properly
    solution: adjust hyperparameters or use a different algorithm (ppo instead of dqn etc)

# shell commands
  • to train the model:
    python3 "/Users/teodoraalexandranitu/Moon landing/moon_landing.py"
  • 
