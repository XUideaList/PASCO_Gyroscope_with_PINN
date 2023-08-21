# PASCO_Gyroscope_with_PINN
From the data obtained during the experiment originally from PASCO's gyroscope experiment, I have used classification(supervised learning) and PINN for trajectory prediction. For detail, please refer to the README file

# Machine Learning within this repository
As in the description, I've used supervised learning as the following method to find the value of the momentent of the inertia of the gyroscope with respect to the pivot: I' (This can be hardly found through experiments.) since we have the formula that can generate the trajectory of the gyroscope with respect to time, we can make various trajectories with different I' values that can be used as the training data of our classification model. 
After the proper I' value is found with the classification process, we can apply PINN(Physics Informed Neural Network) to predict the trajectory with respect to time. Since the motion involves two variables: the polar angle and the azimuthal angle, the model constructed using PINN should also consider this too. Refer to the code to see how I've implemented the two-variable PINN model for this case.

# Solving the DE derived using Conservation of Angular Momentum
Note that the motion of equation implemented in this file uses Euler's method, which eventually occurs a significant amount of error.
Hence there is space for improvement using other methods when solving the given differential equation. (For example, Runge Futta 4'th method)
ㄴ Actually this might be the reason of the differnece between our numerical plot and the experimental data. (I'll leave it out untill I get some time)  
