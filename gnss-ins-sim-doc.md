# **gnss-ins-sim**
---
**gnss-ins-sim** is an open-source GNSS + inertial navigation, sensor fusion simulator.  Motion trajectory generator, sensor models, and navigation. 

## Contents


---

## 1 Introduction
---

## 2 Preliminary
---
### 2.1 Coordinate frames

#### 2.1.1 ECEF frame
The ECEF frame is an Earth-Centered, Earth-Fixed reference system. Its origin is the Earth’s CoM. Its z axis points to the true north. Its x axis points to the intersection of the Greenwich meridian and the equator, and its y axis complete the right-handed coordinate frame. We use the WGS-84 reference ellipsoid in the simulation since it is used in GPS.
Obviously, the ECEF is not an inertial reference system.

<div align=center><img width="500"  src="https://github.com/dxg-aceinna/gnss-ins-sim-doc/blob/master/images/ECEF.png"/></div>

#### 2.1.2 NED frame
For a device near or on the surface of the Earth, it is more convenient to describe its motion (especially rotations) relative the NED (North-East-Downward) or ENU (East-North-Upward) frame. We choose the NED frame in gnss-ins-imu.
Its origin is fixed at the device. Its x axis is in the local horizontal plane and point to the true north. Its z axis is perpendicular to the local horizontal plane and point downwards, and its y axis completes the right-handed coordinate frame.

<div align=center><img width="400"  src="https://github.com/dxg-aceinna/gnss-ins-sim-doc/blob/master/images/NED.png"/></div>

#### 2.1.3 Virtual Inertial frame
For local-area or short-time applications, it may be more convenient to choose a virtual inertial frame as the reference frame especially when the sensor is of low accuracy. In these cases, the shape and rotation of the Earth will be ignored.
The virtual inertial frame can be considered as an NED frame fixed at a known point.

#### 2.1.4 Body frame
The body coordinate system is fixed at the device. Its origin is located at the center of device. Its x axis points forward, lying in the symmetric plane of the device. Its y axis points to the right side of the device. Its z axis points downward to complete the right-hand coordinate system.

## 3 Sensor model
### 3.1 Gyroscope
<div align=center>
<img src="https://latex.codecogs.com/gif.latex?\omega_m=\omega&plus;b_{\omega}&plus;n_{\omega}" title="\omega_m=\omega+b_{\omega}+n_{\omega}" />
</div>

<div align=center>
<img src="https://latex.codecogs.com/gif.latex?b_{\omega}=b_{\omega c}&plus;b_{\omega v}" title="b_{\omega}=b_{\omega c}+b_{\omega v}" />
</div>

<div align=center>
<img src="https://latex.codecogs.com/gif.latex?b_{\omega}_v=n_{\omega v}" title="b_{\omega v}=n_{\omega v}" />
</div>

<div align=center>
<img src="https://latex.codecogs.com/gif.latex?\dot{b}_{\omega&space;v}=\frac{1}{\tau}b_{\omega&space;v}&plus;n_{\omega&space;v}" title="\dot{b}_{\omega v}=\frac{1}{\tau}b_{\omega v}+n_{\omega v}" />
</div>

#### 3.1.1 Constant Bias
For a rate gyro, its bias is the average output from the gyroscope when it is not undergoing any rotation. When the rate gyro output is integrated to get angles, the constant bias causes the angles to grow linearly with time.

#### 3.1.2 White Noise / Angle Random Walk
#### 3.1.3 Bias Stability
#### 3.1.4 Calibration Errors
### 3.2 Accelerometer
#### 3.2.1 Constant Bias
#### 3.2.2 White Noise / Velocity Random Walk
#### 3.2.3 Bias Stability
#### 3.2.4 Calibration Errors
### 3.3 GPS
### 3.4 Magnetometer
## 4 Algorithm
## 5 Sim


