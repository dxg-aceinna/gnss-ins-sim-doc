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

<div align=center><img width="500" src="https://github.com/dxg-aceinna/gnss-ins-sim-doc/blob/master/images/ECEF.png"/></div>

#### 2.1.2 NED frame
For a device near or on the surface of the Earth, it is more convenient to describe its motion (especially rotations) relative the NED (North-East-Downward) or ENU (East-North-Upward) frame. We choose the NED frame in gnss-ins-imu.
Its origin is fixed at the device. Its x axis is in the local horizontal plane and point to the true north. Its z axis is perpendicular to the local horizontal plane and point downwards, and its y axis completes the right-handed coordinate frame.

<div align=center><img width="500 src="https://github.com/dxg-aceinna/gnss-ins-sim-doc/blob/master/images/NED.png"/></div>

#### 2.1.3 Virtual Inertial frame
#### 2.1.4 Body frame
## 3 Sensor model
### 3.1 Gyroscope
#### 3.1.1 Constant Bias
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


