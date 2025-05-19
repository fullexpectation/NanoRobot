这是两轮差速小车rviz和gazebo仿真代码
```bash
ros2 launch cpp06_urdf gazebo_sim.launch.py 
```
```bash
ros2 launch car_navigation2 navigation2.launch.py 
```
```bash
ros2 launch autopartol _robot autopartol.launch.py
```
---------------

打开rviz小车模型
```bash
ros2 launch cpp06_urdf display.launch.py model:=`ros2 pkg prefix --share cpp06_urdf`/urdf/xacro/car.urdf.xacro
```
---------------
使用slam_toolbox建图
```bash
sudo apt install ros-humble-slam-toolbox

```
```bash
ros2 launch slam_toolbox online_async_launch.py use_sim_time:=True
```
rqt
```bash
sudo apt install ros-humble-nav2-map-server
```
保存地图
```bash
ros2 run nav2_map_server map_saver_cli -f room
```
------------------
