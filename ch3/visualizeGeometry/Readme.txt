1. How to compile this program:

* use pangolin: slambook/3rdpart/Pangolin or download it from github: https://github.com/stevenlovegrove/Pangolin

* install dependency for pangolin (mainly the OpenGL): 
sudo apt-get install libglew-dev

* compile and install pangolin  //本机采用方法：先安装git，然后 $ git clone https://github.com/stevenlovegrove/Pangolin.git
cd [path-to-pangolin]           //cd Pangolin（注意：大写开头）
mkdir build                     //其他不变
cd build
cmake ..
make 
sudo make install 

* compile this program:         //注意：此处需要cd到visualizeGeometry，而非在Pangolin/build中进行
mkdir build
cd build
cmake ..
make 

* run the build/visualizeGeometry

2. How to use this program:

The UI in the left panel displays different representations of T_w_c ( camera to world ). It shows the rotation matrix, tranlsation vector, euler angles (in roll-pitch-yaw order) and the quaternion.
Drag your left mouse button to move the camera, right button to rotate it around the box, center button to rotate the camera itself, and press both left and right button to roll the view. 
Note that in this program the original X axis is right (red line), Y is up (green line) and Z in back axis (blue line). You (camera) are looking at (0,0,0) standing on (3,3,3) at first. 

3. Problems may happen:
* I found that in virtual machines there may be an error in pangolin, which was solved in its issue: https://github.com/stevenlovegrove/Pangolin/issues/74 . You need to comment the two lines mentioned by paulinus, and the recompile and reinstall Pangolin, if you happen to find this problem. 

If you still have problems using this program, please contact: gaoxiang12@mails.tsinghua.edu.cn
