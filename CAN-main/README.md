# CAN
Niro Control Area Network </br>

sudo apt-get install libsdl2-dev #need to install if you want to control with joystick </br>

sudo ip link set can1  up type can bitrate 500000 </br>
roslaunch can_package run.launch </br>


