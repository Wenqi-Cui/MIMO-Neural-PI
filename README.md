# Structured Neural-PI Control with End-to-End Stability and Output Tracking Guarantees
This repository contains source code necessary to reproduce the results presented in the following paper:
Structured Neural-PI Control with End-to-End Stability and Output Tracking Guarantees




# Motivation
We study the optimal control of multiple-input and multiple-output dynamical systems via the design of neural network-based controllers with stability and output tracking guarantees. While neural network-based nonlinear controllers have shown superior performance in various applications, their lack of provable guarantees has restricted their adoption in high-stake real-world applications. This paper bridges the gap between neural network-based controllers and the need for stabilization guarantees. Using equilibrium-independent passivity, a property present in a wide range of physical systems, we propose neural Proportional-Integral (PI) controllers that have provable guarantees of stability and zero steady-state output tracking error. The key structure is the strict monotonicity on proportional and integral terms, which is parameterized as gradients of strictly convex neural networks (SCNN). We construct SCNN with tunable softplus activations, which yields universal approximation capability and is also useful in incorporating communication constraints. In addition, the SCNNs serve as Lyapunov functions, giving us end-to-end performance guarantees. Experiments on traffic and power networks demonstrate that the proposed approach improves both transient and steady-state performances, while unstructured neural networks lead to unstable behaviors.




# Language and Dependencies
All code are implemented in Python and can be run through Jupyter notebook (or other equivalent environment such as Google Colab). .
Data for the power system is imported from MATLAB as 'IEEE_39bus_Kron.mat'. We used the open-source Python package Tensorflow 2.0 to implement RNN and train the neural network models.


