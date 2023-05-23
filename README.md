# Structured Neural-PI Control with End-to-End Stability and Output Tracking Guarantees
This repository contains source code necessary to reproduce the results presented in the following paper:
Structured Neural-PI Control with End-to-End Stability and Output Tracking Guarantees




# Motivation
We study the optimal control of multiple-input and multiple-output dynamical systems via the design of neural network-based controllers with stability and output tracking guarantees. While neural network-based nonlinear controllers have shown superior performance in various applications, their lack of provable guarantees has restricted their adoption in high-stake real-world applications. This paper bridges the gap between neural network-based controllers and the need for stabilization guarantees. Using equilibrium-independent passivity, a property present in a wide range of physical systems, we propose neural Proportional-Integral (PI) controllers that have provable guarantees of stability and zero steady-state output tracking error. The key structure is the strict monotonicity on proportional and integral terms, which is parameterized as gradients of strictly convex neural networks (SCNN). We construct SCNN with tunable softplus activations, which yields universal approximation capability and is also useful in incorporating communication constraints. In addition, the SCNNs serve as Lyapunov functions, giving us end-to-end performance guarantees. Experiments on traffic and power networks demonstrate that the proposed approach improves both transient and steady-state performances, while unstructured neural networks lead to unstable behaviors.


# Flexible non-linear controller with stability and output tracking guarantees
Here we show the performance on stablizing inverted pendulum to track the angle of 0.5 rad

https://github.com/Wenqi-Cui/MIMO-Neural-PI/assets/70600351/57330aa0-253e-4b64-9478-789104607d69

By contrast, unstructured neural network fail to stablize the pendulum

https://github.com/Wenqi-Cui/MIMO-Neural-PI/assets/70600351/47f50812-18e3-4e63-9fb5-8611a1a6318f



# Language and Dependencies
All code are implemented in Python and can be run through Jupyter notebook (or other equivalent environment such as Google Colab). The code can also be copied to Google Colab using this [link](https://colab.research.google.com/drive/1vinnX16zuRR0I13ofpopk61zFeTMfwbK?usp=sharing/).
Data for the power system is imported from MATLAB as 'IEEE_39bus_Kron.mat'. The coeffcient for linear droop control is obtained by fmincon function of Matlab as 'Sol_linear.mat'. We used the open-source Python package Tensorflow 2.0 to implement RNN and train the neural network models.


