標籤: #ROS 

---

# Install

安裝 hector slam 可以用 `apt-get` 來完成

```bash
$ sudo apt-get install ros-noetic-hector-slam
```

他會被安裝到

```
/opt/ros/noetic/share/hector_slam_launch
```

# Launch File

```bash
$ roslaunch hector_slam_launch tutorial.launch
```

for [[YDLiDAR X4]]:

```bash
$ roslaunch ydlidar_ros_driver X4.launch
```

> 使用前記得更改 `/opt/ros/noetic/share/hector_mapping/launch` 裡面的參數，譬如如果沒有要用到 odometry 的話要改以下參數
> - `base_frame` 的參數改成 `base_frame`
> - `odom_frame` 的參數改成 `base_frame`
> - `use_tf_scan_transformation` 的參數改成 `false`

> 如果有跳出 timer 的問題，要進去 `/opt/ros/noetic/share/hector_slam_launch/launch/tutorial.launch` 裡面更改 `/use_sim_time` 的參數
> 因為 `tutorial.launch` 有提供載入掃描過程檔案並進行模擬的功能（不需要用到光達），因此才會有這個參數
> 這個功能的使用可以在 [How to build a map using logged data - ROS wiki](https://wiki.ros.org/hector_slam/Tutorials/MappingUsingLoggedData) 中找到

---

參考資料:

[How to set up Hector slam - ROS wiki](https://wiki.ros.org/hector_slam/Tutorials/SettingUpForYourRobot)
[How to build a map using logged data - ROS wiki](https://wiki.ros.org/hector_slam/Tutorials/MappingUsingLoggedData)

---

link:

