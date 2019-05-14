# mpu6050_6dof

test video https://www.youtube.com/watch?v=oLpSd0Yygnk

### Step 1 install mpu6050_serial_to_imu

```bash
sudo apt-get install ros-kinetic-serial
export CATKIN_WS=~/catkin_ws
mkdir -p $CATKIN_WS/src ###如果之前沒有建立才使用
cd $CATKIN_WS/src
git clone https://github.com/fsteinhardt/mpu6050_serial_to_imu
cd ..
rosdep install --from-paths src --ignore-src
catkin_make
```


### Step 2

```bash
ls /dev/ttyUSB*
sudo chmod a+rw /dev/ttyUSB0
roslaunch mpu6050_6dof imu_demo.launch
```
