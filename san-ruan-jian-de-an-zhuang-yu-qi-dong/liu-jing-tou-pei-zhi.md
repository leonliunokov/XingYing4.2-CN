# （六）镜头配置

**设备初始化**

1. 即插即用镜头通电后数码管会显示000​（设备初始化状态代码），打开软件后会自动分配IP地址，IP地址从201起顺序分配，若存在标定文件，则从标定记录中最后一个设备序列号+1开始分配；

**设备发现与设备状态**

1. 打开软件后设备列表会显示待连接设备IP，连接镜头后，将鼠标悬浮在设备状态栏可查看详细信息：

* 主镜头：用于同步信号输出
* 镜头：标定/未标定
*   连接状态：连接/丢帧/离线\


    <figure><img src="../.gitbook/assets/image (489).png" alt="" width="375"><figcaption></figcaption></figure>



    <figure><img src="../.gitbook/assets/image (488).png" alt="" width="375"><figcaption></figcaption></figure>

**IP地址修改功能**

1. 操作方式：软暂停视频播放后在设备管理界面，右键选中目标设备 → 选择【编辑IP】，双击设备IP字段进入手动修改模式，输入符合规范的IP地址；

{% hint style="warning" %}
保存要求：修改后必须执行【保存标定文件】，否则重启软件后IP将恢复标定文件中记录的IP
{% endhint %}

**主镜头设置**

1.  操作方式：软件暂停播放，右键点击已连接的设备，选择【设为主镜头】，系统将自动更新主镜头标识并同步信号源；\


    <figure><img src="../.gitbook/assets/image (490).png" alt="" width="375"><figcaption></figcaption></figure>
