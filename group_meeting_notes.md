## Next meeting - Meg and Patrick: ???
- Schedule two weekly meetings
- Schedule office hours with Dr. White
- Show flight data and buoy data to Patrick
- Discuss github repo
  - best practices
  - new resources that I have posted
  - repo is now public

## Tuesday, February 11, 2020: Meg and Dr. White
Talked about pros and cons of a couple different approaches:
1. Using a network to simplify/emulate a PDE ocean model so velocity vectors for next time period can be approximated in a computationally efficient manner to be done on-board the glider, rather than by a centralized controller as in the Edwards paper
  - the system of PDEs might not describe the ocean currents well, especially because we have strong tidal flow and the gulf stream causing eddies and weird stuff at long bay (which I guess is hard to model well using PDEs?)
1. Using an autoregressive model with the measured velocity vector time series as input with original glider position, planned path/objective, potentially some info from a physical model as covariates
  - Could predict the velocity vector at the next stemp and potentially use difference between predicted velocity vector and velocity vector measured at the next time step for reinforcement learning
  - Could also directly compute optimal control scheme for next time period and optimize over energy consumption as well as closeness to preferred path
  - or both in some 2-step network(s)

#### Resources to explore
- Sergey levin - Berkley:
  - Reinforcement learning for controls, teaching robots stuff
  - Does a great job explaining RL and autoregression
- DeepAR
  - autoregressive model toolkit?

   
