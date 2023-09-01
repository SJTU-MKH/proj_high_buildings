# 多楼宇配送机器人应用场景

## world搭建
使用gazebo模型库中的parking_garage放置两栋楼，贴一层地形，保存生成building3.world

## 运行
1. 修改scout_simulator/scout_gazebo_sim/launch/scout_empty_world.launch中world_name默认值为保存的world名字
2. 编译 `catkin_make`
   1. 键盘控制接口：`sudo apt install ros-melodic-teleop-twist-keyboard `
   2. gazebo joint 控制依赖:`sudo apt install ros-melodic-velocity-controllers`
3. `source devel/setup.zsh`
4. 运行`roslaunch scout_gazebo_sim scout_empty_world.launch`
5. 运行键盘控制接口`roslaunch scout_gazebo_sim scout_empty_world.launch`

## 注意
- 看到的地面地形会闪，是因为ground_plane存在，删去就不会闪了