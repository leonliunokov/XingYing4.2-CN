# （十二）Ros2与Nokov的通信

## **软件的安装与设置**

### **软件安装**

* 软件安装步骤请参考“三、软件的安装与启动”

### **VRPN功能**

* 关于 VRPN 的使用方法以及相关插件，请参考“六、视图介绍--（三）数据广播--VRPN 广播数据”。

### **启动 VRPN 服务获取数据**

1. 在实时模式下播放，快速创建一个 Markerset，或者在后处理模式下加载带有Markerset的数据，Markerset 的创建方法请参考“九、创建Markerset”。
2. 在XINGYING软件打开数据广播面板开启 VRPN ，VRPN的功能介绍参考“六、视图介绍--（三）数据广播--VRPN 广播数据”
3. 可以运行测试程序“NokovVrpnClient.exe”来获取动捕数据（具体操作参考“六、视图介绍--（三）数据广播--VRPN 广播数据”），若无法收到数据，请检查 XINGYING 中的 VRPN 配置和 数据广播的IP 地址是否正确。（如有需要，“NokovVrpnClient.exe”可执行测试程序，请咨询技术工程师获取）；

***

## **安装Ros2**

### **版本说明**

1. 安装的 Ros2 版本：foxy，Ubuntu 版本：20.04。通过 XINGYING 软件,使用 VRPN 将动捕的 Markerset 或者刚体等数据传给 Ros2。
2. 启动 Nokov 虚拟机，打开终端，依次输入以下命令：
   * sudo apt install ros-foxy-desktop；
   * sudo apt install ros-foxy-vrpn；
   * source /opt/ros/foxy/setup.bash；
   * cd \~/ros2\_ws/src；
   * git clone -b foxy-devel https://github.com/NOKOV-MOCAP/vrpn\_client\_ros；
   * cd \~/ros2\_ws；
   * colcon build --packages-select vrpn\_client\_ros --symlink-install；
   * source install/setup.bash；
3.  进 入 路 径 ： ros2\_ws/src/vrpn\_client\_ros/config ， 输 入 gedit sample.params.yaml按下回车键，服务器的 IP 地址是“192.168.0.107”, 将服务器的 IP 地址修改为 XINGYING 设置的网卡广播地址，保存文件后退出。\


    <figure><img src="../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

### **启动 vrpn\_client\_ros**

1. 开 启 一 个 终 端 ， 在 每 次 开 启 终 端 后 ， 需 要 输 入 “ source /opt/ros/foxy/setup.bash”指令
2.  继续输入命令：“ros2 launch vrpn\_client\_ros sample.launch.py  ”按下回车键。终端中打印出“Connection established”、“Found new sender: Tracker2”、 “Creating new tracker Tracker2”这三行，说明连接成功和动捕成功建立了通讯，并且 Ros2 已经获取到了动捕数据，“Tracker2”表示 XINGYING 软件中 Markerset 的名称；\


    <figure><img src="../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>
3.  在启动 vrpn\_client-ros 中需要注意，IP 地址设置一定要对，要和 XINGYING

    软件主机位于同一网段，能 ping 通。

### **话题订阅与查询**

1.  打开一个终端，查看 topic 话题。输入命令”ros2 topic list”可以看到话题“/Tracker0/pose”，“   Tracker0”表示 XINGYING 软件中 Markerset 的名称；\


    <figure><img src="../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>
2. 输入命令“ros2 topic echo /Tracker0/pose”按下回车后可以看到接收到的数据，“Tracker0”表示 XINGYING 软件中 Markerset 的名称；
3.  数据说明：“Pose”表示 Markerset 的位置方向，Pose”下的“Positition”表示 Markerset 的位置信息，“orientation”表示 Markerset 的方向旋转信息。只有勾选了“刚体”类型的时候，Ros2 中才会打印出“orientation”的数据， 勾选“标记点、标记点(未命名)”类型“orientation”不会打印数据。\


    <figure><img src="../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>





***

## **ROS 与VRPN 功能使用说明**

### **VRPN 功能的三种类型**

1. 在数据广播中开启 VRPN，VRPN 可分为三种类型:刚体、标记点、标记点(未命名)。
2.  在勾选 VRPN 各个功能以及修改值之前，请先将软件暂停播放，在数据广播中取消勾选“启用 VRPN”后再进行功能的勾选和值的修改，在勾选好功能后请勾选上“启用 VRPN”并将软件播放。\


    <figure><img src="../.gitbook/assets/image (452).png" alt=""><figcaption></figcaption></figure>
3. 刚体类型
   * 刚体类型表示发出刚体的信息数据。在 XINGYING 中快速创建一个刚体，选择“刚体”类型，开启 VRPN，播放动捕软件。在 Ros2 的终端输入“ros2 launch vrpn\_client\_ros sample.launch.py ”，获取到动捕数据后，打开另一个终端输入”ros2 topic list”,可以看到终端中打印出的刚体的话题，输入“ros2 topic echo+话题名称”，终端中会打印该话题的数据；
4. 标记点类型
   *   标记点类型勾选时表示发出有名称的 Marker 点信息数据。创建 Mrakerset 后选择“标记点”类型，开启 VRPN，播放动捕软件，在 Ros2 终端输入命令启动 Ros2，获取到动捕数据后打开另一个终端输入命令订阅标记点话题， “Tracker0\_Marker1”中的“Tracker0”表示 Markerset 名称，“Marker1”表示 Markerset 的第一个点的名称，若需要获取 Markerset 的第二个点的数据， 只需要将“Marker1”更改为“Marker2”，以此类推 ，输入命令“ros2 topic echo /Tracker0\_Marker1/pose”回车后，可以看到“Tracker0”的“Marker1” 这个点的数据了；\


       <figure><img src="../.gitbook/assets/image (453).png" alt=""><figcaption><p><br></p></figcaption></figure>

       <figure><img src="../.gitbook/assets/image (455).png" alt=""><figcaption></figcaption></figure>
5. “标记点(未命名)”
   *   标记点(未命名)表示发出未命名的 Marker 点信息数据。选择“标记点(未命名)”类型，开启 VRPN，播放动捕软件。在 Ros2 终端输入命令启动 Ros2， 获取到动捕数据后打开另一个终端输入命令订阅未命名点话题，输入命令“ros2 topic echo /U\_Tracker0/pose”回车后，终端中会打印未命名点的数据。“U\_Tracker0”表示第一个未命名点，若要获取第二个未命名点的信息数据，可以将“U\_Tracker0”改为“U\_Tracker1”，表示第二个未命名点。\


       <figure><img src="../.gitbook/assets/image (456).png" alt=""><figcaption></figcaption></figure>

       <figure><img src="../.gitbook/assets/image (457).png" alt=""><figcaption></figcaption></figure>

### **单位与反转**

1.  在单位下拉框中可以更换不同单位，分为“毫米、厘米、米”，将动捕暂停

    →打开数据广播，在单位下拉框中选择要更换的单位→开启 VRPN→点击播放。更换单位后，Ros2 中打印的“Position”数据的单位也会实时改变，可搭配 VRPN 的三种类型使用；
2. 在“反转”中勾选上“X、Y、Z“，表示将 VRPN 三种类型的位置数据的正负号反转，若勾选前在 Ros2 中“Position”的数据为正，勾选后则会变为负。勾选后会将 Ros 中的“Position”的 X、Y、Z 坐标数据反转；
3. “qx、qy、qz”表示方向旋转数据的反转，勾选后会将 Ros2 中 的“orientation”的 X、Y、Z 坐标数据反转。

### **位置偏移**

* 在“偏移”中可以设置变量数据的“X、Y、Z”坐标偏移（如图 29），将软件暂停播放→打开数据广播→在“偏移”值输入框中修改 X、Y、Z 的坐标偏移→开启 VRPN→点击播放。修改好坐标偏移的值后，在 Ros2 中会将修改的值加到“Position”的 X、Y、Z 坐标值上。

### **速度和加速度**

1. 在 XINGYING 软件中勾选“速度”后，在 Ros2 终端输入命令获取话题，“twist”表示速度，输入命令“rostopic echo /Tracker4/twist”按下回车，终端中便会打印“Tracker4”这个刚体的的速度的数据信息了；
2. 在XINGYING 软件中勾选“加速度”后，在Ros2 终端输入命令获取话题，“accel”表示加速度，输入命令“rostopic echo /Tracker4/accel”按下回车，终端中便会打印“Tracker4”这个刚体的加速度的数据信息了；
3. Frames 表示帧因子，该值用于速度计算，可在下拉框调节该值使实际速度值与输出的速度值接近。
