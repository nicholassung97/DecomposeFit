# Decomposition of the fit function

In tensorflow, the model is usually first created by defining the layers, activation functions, initialisation of weights, etc. Next, the model is configured with the optimzer, losses and metric with the ```model.compile()``` function. Thereafter, we can train the model with the ```model.fit()``` function. 

This in repository, the intention is to unwrap the ```model.fit()``` function. The purpose for this is to extract and analyse the interference between gradient task in multitask optimsation landscape. In this example, we will be analysing the gradient interference in physics-informed neural network (PINNs). 

In PINNs, the loss function includes both the error produced from the boundary/ initial conditions and the error from the partial differential equation.

![alt text](https://www.researchgate.net/profile/Zhen-Li-105/publication/335990167/figure/fig1/AS:806502679982080@1569296631121/Schematic-of-a-physics-informed-neural-network-PINN-where-the-loss-function-of-PINN.ppm)


