# Arrhenius

Arrhenius.jl is a differentiable combustion simulation package built with the design principle of treating auto-differentiation as a first-class citizen. It aims to facilitate the development of hybrid physics and AI models, paving the way for advancements in automonous combustion research. This README offers a detailed overview of the project, including installation instructions, related publications, applications, and more.

## Installation

To install Arrhenius.jl, enter the following command:
  
```julia
pkg> add https://github.com/DENG-MIT/Arrhenius.jl
```

## Publication

+ [Arrhenius.jl: A Differentiable Combustion Simulation Package](https://arxiv.org/pdf/2107.06172.pdf): overview of Arrhenius.jl and applications in deep mechanism reduction, uncertainty quantification, mechanism tuning and model discovery. [Slides in NCM21](https://www.slideshare.net/WeiqiJi/arrheniusjl-a-differentiable-combustion-simulation-package-248457895), [Vedio for NCM21](https://www.youtube.com/watch?v=X1mwpW78NvA).
+ [Machine Learning Approaches to Learn HyChem Models](https://www.researchgate.net/publication/350890609_Machine_Learning_Approaches_to_Learn_HyChem_Models): demonstrate 1000 times faster than genetic algorithms using commercial software for optimizing complex kinetic models.
+ [Neural Differential Equations for Inverse Modeling in Model Combustors](https://www.researchgate.net/publication/351223124_Neural_Differential_Equations_for_Inverse_Modeling_in_Model_Combustors)
+ [SGD-based Optimization in Modeling Combustion Kinetics: Case Studies in Tuning Mechanistic and Hybrid Kinetic Models](https://doi.org/10.1016/j.fuel.2022.124560)

## Application

+ **Sensitivity analysis for auto-ignition** | [repo](https://github.com/DENG-MIT/ArrheniusActiveSubspace) | Features: auto-differentiation, multi-threading, sensitivity to all of three Arrhenius params A, b and Ea, active subspace based uncertainty quantification
+ **Sensitivity analysis for one-dimensional flames** | [repo](https://github.com/DENG-MIT/Arrhenius_Flame_1D) | Features: auto-differentiation, multi-threading, sensitivity to all of three Arrhenius params A, b and Ea.
+ **Automonous learn kinetic mechanism using neural network** | [repo](https://github.com/DENG-MIT/CRNN_HyChem) | Features: Chemical Reaction Neural Network (CRNN), Neural Ordinary Differential Equations.
+ **Deep Reduction** | [repo](https://github.com/DENG-MIT/DeepReduction) | Features: Two-stages mechanism reduction with deep learning.

**Example**

> Note that some of the examples are in development and you can have early access by contacting [Weiqi Ji](mailto:weiqiji@mit.edu)

+ [Pyrolysis of JP10](./example/pyrolysis/pyrolysis.ipynb)
+ [Perfect Stirred Reactor](./example/perfect_stirred_reactor)
+ [Auto-ignition](https://github.com/DENG-MIT/NN-Ignition)
+ [Compute Jacobian using AD](https://gist.github.com/jiweiqi/21b8d149bd95b97d9ae948ab92e446df)

## Relevent package

+ [ReactionMechanismSimulator.jl](https://github.com/ReactionMechanismGenerator/ReactionMechanismSimulator.jl) The amazing Reaction Mechanism Simulator for simulating large chemical kinetic mechanisms
+ [Cantera](https://cantera.org/) A comprehensive C++ based combustion simulation package and with great python interface. Arrhenius relies on Cantera when it is applicable.
