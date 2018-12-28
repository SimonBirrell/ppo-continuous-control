# Proximal Policy Optimization on a Unity Environment
*Solution to the second project on the Udacity Deep Reinforcement Learning Course*

## Introduction
This repo contains my solution to the second project in the Udacity Deep Reinforcement Learning Course: Continuous Control. The Unity enviornment contains 20 robotic arms that all follow the same policy. Their task is to learn to track some moving globes with their end effectors.

A reward of 0.1 is given for each timestep that the end effector coincides with the target position. 
The state space consists of 33 real numbers, corresponding to position, rotation, velocities and angular velocities of the two arm links.
The action spaces consists of 4 real numbers, corresponding to the torques applied to each of the two joints.

The trigger for the end of an episode is not documented, but appears to be around every 1000 time steps.

At the end of each episode, the average total reward for all the agents is taken. This average is then tracked from episode to episode. The trailing average of these averages over the last 100 episodes must exceed 30.0 for the environment to be considered solved.

## Installation

To set up your python environment to run the code in this repository, follow the instructions below.

1. [Download and install Anaconda](https://www.anaconda.com/download/), if you don't already have it.


2. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```
	
3. Clone the repository and navigate to the root folder.  Then, install several dependencies.
```bash
git clone https://github.com/SimonBirrell/ppo-continuous-control-project.git
cd ppo-continuous-control-project
pip install .
```

4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

5. Run the notebook
```bash
jupyter notebook Navigation.ipynb
```

6. Before running the code in the notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. You should only need to do this the first time. 

7. Download the Unity environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

8. Place the file in the root directory of this repository and unzip (or decompress) the file. 

9. Run the code (by clicking the top cell and then using Shift-Enter to execute each cell in turn) right down to and including the "It's Your Turn" cell. This should solve the environment in under 300 episodes. Make sure the Unity window is visible, as otherwise the simulation has atendency to pause itself.

10. To see the trained agent, then run the cell titled "Run the policy".



