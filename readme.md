# 运行
roslaunch fast_lio_sam avia_debug.launch

# 保存轨迹
rosservice call /save_pose "resolution: 0.0 destination: ''" 
# 保存地图
rosservice call /save_map "resolution: 0.0 destination: ''" 
# 轨迹评估
evo_traj kitti optimized_pose.txt without_optimized_pose.txt  -p
