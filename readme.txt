AUTHORS:
MIGUEL ANGEL SILVA PLATA
NAYARA CARMINIA LARA RAMOS

DEMO OF VIDEOS IN DRIVE: https://drive.google.com/drive/folders/1ZSOvwGtamnbumQAMcbsiqwPMuvc-I0sJ

PART 1 -----------------index test ws-----------------------------------------
Index Finger proceedings ----------------------------------------

---Terminal 1:
colcon build
source install/setup.bash
ros2 launch robot_description view_robot.launch.py use_jsp:=false gui:=false

---Terminal 2:
colcon build
source install/setup.bash
ros2 run visual_pubsub inverse_kinematics


Thumb Finger proceedings -------thumb test ws---------------------------------

---Terminal 1:
colcon build
source install/setup.bash
ros2 launch robot_description view_robot.launch.py use_jsp:=false gui:=false

---Terminal 2:
colcon build
source install/setup.bash
ros2 run visual_pubsub inverse_kinematics

NOTE: As mentioned by the proffesor, sometimes it wont work at first, the commands might needed to be run again.

NOTE: Some examples are shown in video linked with the repository.

PART 2 ---------------------------Robotics P ws-------------------------------
Nodes Comm proceedings

STEP 1: Extract the workspace from the repository.
STEP 2: Open “Terminator” and split the window vertically into two panes.
STEP 3: Open the “Robotics_P_ws” workspace.
STEP 4: Enter the command “colcon build” in the workspace. 
STEP 5: Enter the command “source install/setup.bash” in the terminal
STEP 6: Enter the command “ros2 launch ej2pubsub system.launch.py” in the terminal to start executing the code and observe the sending and receiving of data
STEP 7: On the second terminator screen, run “colcon build” followed by “source install/setup.bash”.
STEP 8: In the same window, open “rqt_graph” to view the communication between our nodes and topics.
STEP 9 (OPTIONAL): Run the command “ros2 topic echo topic_name” with the topics:
- /SENSOR_1
- /SENSOR_2
- /SENSOR_3
- /FILTERED_SENSOR
EXTRA --------------------------------both ws --------------------------

---Terminal 1:
colcon build
source install/setup.bash
ros2 launch robot_description view_robot.launch.py use_jsp:=false gui:=false

---Terminal 2:
colcon build
source install/setup.bash
ros2 run visual_pubsub inverse_kinematics


Both index and thumb fingers are shown:
the reach point is inveerse transformed for both frames O and L to work in the absolute frame O, the thumb reach position is then transformed by ([OL])^-1 to work with the same equations as the excercise previously mentioned.
