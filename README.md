# Decomposition of the fit function

In tensorflow, the model is usually first created by defining the layers, activation functions, initialisation of weights, etc. Next, the model is configured with the optimzer, losses and metric with the ```model.compile()``` function. Thereafter, we can train the model with the ```model.fit()``` function. 
This in repository, the intention is to unwrap the ```model.fit()``` function. The purpose for this is to extract and analyse the interference between gradient task in multitask optimsation landscape. In this example, we will be analysing the gradient interference in physics-informmed neural network.
