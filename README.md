robot_localization
==================
Documentation for package : http://docs.ros.org/melodic/api/robot_localization/html/index.html

Changes Done in IGVC_2022 :
A plugin has been created to publish odometry data for base_link for vehicle under igvc_self_drive_description urdf sensors imu.urdf.xacro
    <gazebo>
      <plugin name="p3d_base_controllers" filename="libgazebo_ros_p3d.so">
        <alwaysOn>true</alwaysOn>
        <updateRate>50.0</updateRate>
        <bodyName>base_link</bodyName>
        <topicName>odom</topicName>
        <gaussianNoise>0</gaussianNoise>
        <frameName>world</frameName>
        <xyzOffsets>0 0 0</xyzOffsets>
        <rpyOffsets>0 0 0</rpyOffsets>
      </plugin>
    </gazebo>
    
 Gaussian Noise has been set all 0 values in gps.urdf.xacro
 
1)To run Above package you need to run odom_frameid.py file seperately under scripts to change frame_id of gazebo generated odometry message
2) Now run the launch file to test ekf (parameters has been changed necessiarily according to gazebo simulation in param foilder)
