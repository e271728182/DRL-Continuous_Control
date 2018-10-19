# DRL-Continuous_Control
Second Assignment of DRL

DDPG algorithm trained on the reacher environment of Unity

This reportory contains files used to build a deep reinforcement learning network to solve the continuous control task . An agent with double jointed arms must  be maintained in the goal location

Reacher game description
the state space is a vector of 33 dimensions that describe the environment where the agent is. The action space consist of a 3 dimensional vector with continuous values between -1 and 1. the reward is +0.1 for every time step the arm is at the right place


### Description of files used
the 5 files below are used to build & train the models and have dependencies from Pytorch, Numpy, namedTuples,UnityEnvironment,Gym and Collections.

checkpoint_actor.pth.pth : A trained actor for the DDPG model 
checkpoint_critic.pth: A trained critic actor for the DDPG model
Model.py :An actor-critic model build on a  Deep neural network architecture (original from DRL repository)
ModelV02.py:An actor-critic model build on a  Deep neural network architecture with a tentative batch normalization and modified NN parameters.
ddpg_agent2.py: An agent class that implements the DDPG algorithm. Agent class inherits the Qnetwork class in Model.py. this has been modified from the orifinal ddpg_agent.py from the DRL repository

the forward method overrides the nn.module forward method as prescribed in the documentation
the forward method does not need to be called explicitly

Continus_Control.ipynb: A jupyter notebook that connects to Unity environment to run the UnityEnvironment(file_name='/data/Reacher_One_Linux_NoVis/Reacher_One_Linux_NoVis.x86_64'). the notebook contains the function ddpg which is used to train a ddpg network architecture using the state,actions,reward as inputs.

DDGP report: to be completed

#### How to run the model
Everything is self contained in the Continus_Control.ipynb notebook. Simply run every cell and the dqn function will create a trained model as an ouput in the directory. Simply change the name of the output file in the ddpg function to save a new copy

How to set up the dependencies
Detailed instructions are available on Alexis Cook's DRL repository https://github.com/udacity/deep-reinforcement-learning/blob/master/README.md

### additional document to help me navigate the algorithm and its pitfalls
I added a document called 'Udacity assigmment 2 DRL' it contains screenshot on my first attempt using parameters suggested in the review with corresponding (dismal) result. Also attempt2 describes my implementation of batch normalization and the corresponding error mistake I get and don't understand why

