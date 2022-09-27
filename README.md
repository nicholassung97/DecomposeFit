# Decomposition of the fit function

In tensorflow, the model is usually first created by defining the layers, activation functions, initialisation of weights, etc. Next, the model is configured with the optimzer, losses and metric with the ```model.compile()``` function. Thereafter, we can train the model with the ```model.fit()``` function. 

This in repository, the intention is to unwrap the ```model.fit()``` function. The purpose for this is to extract and analyse the interference between gradient task in multitask optimsation landscape. We will be analysing the gradient interference in physics-informed neural network (PINNs). 

In PINNs, the loss function includes both the error produced from the boundary/ initial conditions and the error from the partial differential equation.

<img src="https://github.com/nicholassung97/DecomposeFit/blob/main/Schematic-of-a-physics-informed-neural-network-PINN-where-the-loss-function-of-PINN.pbm" width="450" height="300">

This two components in the loss function of PINNs can therefore reshaped PINNs into a multitask learning problem. Hence, we will analyse the task gradient wrt each of the respective loss components.

The Google Colab notebook for the decomposition of ```model.fit()``` and extraction and analysis of the interference between gradient task of the two loss terms can be found here.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/nicholassung97/DecomposeFit/blob/main/change_fit_function_draft2(cos_similarity).ipynb)

# Results

The results show the the gradients are mostly orthogonal, need to be subjected to further analysis.
