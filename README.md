# SC-LIO-SAM_based_relocalization
Scan Context is used to get initial guess instead of selecting by user in rviz.  
Because SC-LIO-SAM and LIO-SAM_based_relocalization have the same package name，we put them in different workspace.  
(在LIO-SAM_based_relocalization中添加利用scancontext检测确定机器人开机后在地图中的位置，可以代替手动选取初始点位。该方法需要搭配SC-LIO-SAM建图使用。因为SC-LIO-SAM和LIO-SAM_based_relocalization功能包名相同，因此放在两个工作空间下，一个用于建图一个用于重定位。)

## Run the package
1. Make sure the map should be saved in the right folder:
```
Firstly, you need to run SC-LIO-SAM, and then save the map in the default folder
```

2. Run the launch file:
```
roslaunch lio_sam run_relocalize.launch
```

3. Play existing bag files:
```
rosbag play your-bag.bag
```

 -A video of the demonstration of the method can be found on [Bilibili](https://www.bilibili.com/video/BV1f94y1E72i/#reply197352110848)
 ## Notes

  - **Initialization:** During the initialization stage, had better keep the robot still. Or if you play bags, fistly play the bag for about 0.5s, and then pause the bag until the initialization succeed.
  - **Dependency:** Please refer to [LIO-SAM](https://github.com/TixiaoShan/LIO-SAM#dependency) , [SC-LIO-SAM](https://github.com/gisbi-kim/SC-LIO-SAM) and [LIO-SAM_based_relocalization](https://github.com/Gaochao-hit/LIO-SAM_based_relocalization)

******************************************************************************************************************************************************************

