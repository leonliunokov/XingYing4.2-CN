# （二）手柄连接说明与VRPN数据接入UE说明

### **MOCUTE-052F手柄**

1. MOCUTE-052F手柄通过蓝牙的连接方式与电脑连接，手柄连接：将手柄侧面开关拨到 GAME侧之后，操作手柄开机并调节为 AUTO 模式（出厂默认自动AUTO模式），在电脑上打开蓝牙连接上手柄设备。
2. **MOCUTE-052F手柄操作说明：**
   * 开机：按住<img src="../.gitbook/assets/image (245).png" alt="" data-size="line">键，直到指示灯亮起（约2秒钟），系统开机。（先要装入电池）
   * 关机：按住<img src="../.gitbook/assets/image (246).png" alt="" data-size="line">键，直到指示灯熄灭（约5秒钟），系统关机。注意：当开机后没有连接无线设备，5分钟后系统将自动关机；如果有连接无线设备，30分钟没有任何操作，系统也将自动关机
   * 配对连接：开机后，LED指示灯将闪烁，自动进入无线配对模式，查找到手柄的地址及名称（MOCUTE-052F-xxx），点连接即可。连接成功后，LED指示灯熄灭。下次开机将会自动连接到最后配对的无线设备。
   * 取消配对：在关机状态下，开机时按住<img src="../.gitbook/assets/image (247).png" alt="" data-size="line">键超过8秒钟，指示灯将闪烁，此时进入重新配对模式，将不会自动连接上次已配对设备
   * 开机模式（出厂默认自动AUTO模式）手柄在出厂默认为自动AUTO模式，直接按电源键开机显示无线名MOCUTE-x-AUTO\\
3. MOCUTE-052F手柄注意事项：
   * 当意外情况导致无法开机或无法关机，请取出电池后，重新装上。
   * 如果出现不能连接情况，请同时按B+Y+电源键开机，并将摇杆转动两圈（校准）后再关机，恢复出厂设置。
   * 当配对不正常或找不到无线名，手柄关机，按住电源键8秒钟以上灯闪再松开，将设备上无线配对全部取消并忽略，再重新配对。



***

### **动捕设置** <a href="#toc9931" id="toc9931"></a>

* 在软件设置中开启“VRPN”，连接镜头播放。

{% hint style="info" %}
注意：手柄和动捕连接最多同时接入两个手柄，按手柄接入的顺序，手柄名称分别为：“joystick1 ”和 “joystick2”，连接手柄必须和 XINGYING 软件位于同一台电脑。
{% endhint %}

#### &#x20;<a href="#toc18263" id="toc18263"></a>

***

### **连接VRPN** <a href="#toc18263" id="toc18263"></a>

{% hint style="info" %}
注意：在使用“NokovVrpnClient.exe”时请确保XINGYING软件处于播放状态；
{% endhint %}

1.  使用测试工具“NokovVrpnClient.exe”进行手柄连接，在“NokovVrpnClient”文件夹中运行“NokovVrpnClient.exe”，在PowerShell终端中输入“./NokovVrpnClient.exe joystick1@127.0.0.1”（17.2.1），或者在命令提示符中输入“NokovVrpnClient.exe joystick1@127.0.0.1”，按下手柄上的键位或滑动手柄轮盘后终端中会打印出按键对应关系及其数据，当终端中成功响应了手柄的按键后则表示手柄与XINGYING连接成功；\


    <figure><img src="../.gitbook/assets/image (249).png" alt=""><figcaption><p>17.2.1</p></figcaption></figure>
2. 若接入了两个手柄，连接第二个手柄时则在终端中将“joystick1”改为“joystick2”；
3.  按键对应关系（17.2.2）；\


    <figure><img src="../.gitbook/assets/image (248).png" alt="" width="209"><figcaption><p>17.2.2</p></figcaption></figure>
4. 滑块坐标说明：坐标范围为 0-65535，左上分别为 x，y 的起始坐标（0，0）。



***

### **手柄接入UE** <a href="#toc24006" id="toc24006"></a>

1. 在UE中点击“窗口→LiveLink”，在“LiveLink”窗口中添加“LiveLinkVRPN源”，现在我们对手柄的轮盘进行主题添加：
2. 在“Connection Settings”中，“IPAddress”请保持默认不要修改；
3. “Local Updata Rate in Hz”中的帧率与VR Tracker软件设置的帧率保持一致；
4. 在“Device”输入需要连接的手柄名称，如连接第一个手柄时，那么此处就输入“joystick1”；
5. “Subjectname”表示主题命名，“Type”选择“Analog”；
6.  所有参数设置完后点击添加（17.2.3），此时滑动手柄的轮盘，下方便会成功添加出轮盘的主题；选中轮盘的主题名称，在右侧点击“视图选项”，在下拉框中选择“显示帧数据”，将“属性值展开”，滑动手柄的轮盘后属性值会变化（17.2.4）；\


    <figure><img src="../.gitbook/assets/image (250).png" alt=""><figcaption><p>17.2.3</p></figcaption></figure>



    <figure><img src="../.gitbook/assets/image (251).png" alt=""><figcaption><p>17.2.4</p></figcaption></figure>
7.  添加Button(手柄键位)主题：“IPAddress”请保持默认不要修改，“Local Updata Rate in Hz”中的帧率与VR Tracker软件设置的帧率保持一致，在“Device”输入需要连接的手柄名称，如连接第一个手柄时，那么此处就输入“joystick1”，“Subjectname”表示主题命名（注意主题名称请不要与轮盘的主题名称重复），“Type”选择“Button”（17.2.5），点击添加后按下手柄上的键位，主题列表中就会添加上Button主题了。选中Button主题，将属性值展开，此时按下对应键位，“属性值0”会显示出按下的按键的编号，当按键被按下后，“属性值1”的数值会由“0”变为“1”（17.2.5）；\


    <figure><img src="../.gitbook/assets/image (252).png" alt=""><figcaption><p>17.2.5</p></figcaption></figure>





***

### **创建蓝图类** <a href="#toc9772" id="toc9772"></a>

*   在内容浏览器中点击右键，创建一个蓝图类，选择创建一个“Actor”蓝图类，双击此“actor”蓝图，在“我的蓝图→事件Tick”中添加各个节点（17.2.6），注意添加的两个“计算实时链接”的节点后，在该节点的“对象”中请分别选择“Button主题名称”和“轮盘主题名称”（17.2.7）；\


    <figure><img src="../.gitbook/assets/image (253).png" alt=""><figcaption><p>17.2.6</p></figcaption></figure>



    <figure><img src="../.gitbook/assets/image (254).png" alt="" width="449"><figcaption><p>17.2.7</p></figcaption></figure>
*   添加完各个节点后（17.2.8），点击编译、保存。\


    <figure><img src="../.gitbook/assets/image (255).png" alt=""><figcaption><p>17.2.8</p></figcaption></figure>





***

### **在UE场景中使用手柄** <a href="#toc3396" id="toc3396"></a>

*   **在内容浏览器中将“Actor”蓝图类拖入UE场景中，点击播放，此时滑动手柄轮盘或按下各个键位，在UE场景中会显示出Button编号、状态和坐标（17.2.9）。**\


    <figure><img src="../.gitbook/assets/image (256).png" alt=""><figcaption><p>17.2.9</p></figcaption></figure>

#### &#x20;<a href="#toc7002" id="toc7002"></a>

***

### **XBOX 360手柄**

1.  XBOX 360手柄通过USB线连接的方式与电脑连接，将XBOX 360手柄的USB线插入XINGYING软件所在的电脑上，XBOX 360手柄按键对应关系：\


    <figure><img src="../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure>
2. XBOX 360手柄使用和MOCUTE-052F手柄使用方法一致，具体操作说明请阅读上文”十七、手柄连接说明与VRPN数据接入UE说明”中的步骤四\~八；
