# Estimation Project #

This is the estimation portion of the controller used in the CPP simulator.The simulated quad will be flying with your estimator and your custom controller (from the previous project)!

#Tasks

## Step 1: Sensor Noise

After running the simulator in Xcode, logs were created inside config/logs folder. From the measured values, standard deviation of GPS and one accelerometer's x were calculated. 

> MeasuredStdDev_GPSPosXY = 0.7
> MeasuredStdDev_AccelXY = 0.51

![Step 1](stddev.png)
These values seem to tally well with SimulatedSensors.txt values of 0.7 and 0.5




## Step 2: Attitude Estimation
In order to improve the gyro,use the non-linear Euler forward approach. FromEuler123_RPY is a handy method to convert current Euler estimates to a quaternion. Then IntegrateBodyRate is used to integerate the body rate. Finally, convert the quaternion back to new euler angle. Yaw may be normalized to lie in between -pi and pi. 

![Step 2](step2.png)


## Step 3: Prediction Step

## Step 4: Magnetometer Update
## Step 5: Closed Loop + GPS Update
## Step 6: Adding Custom Controller






