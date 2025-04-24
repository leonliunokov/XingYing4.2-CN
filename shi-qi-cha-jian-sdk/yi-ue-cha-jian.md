# （一）UE插件

### **软件设置与人体创建**

1. 打开数据广播面板，开启“SDK”；
2. XINGYING软件已完成标定，在实时模式创建53点人体模型或者在后处理加载一段带有53点人体模型的数据，将软件播放。

***

### **插件安装与UE设置**

1.  根据使用的UE版本，下载对应的NokovLiveLink插件，安装使用方式一致。举例：使用UE\_4.26引擎，请将UE\_4.26引擎的“NokovLiveLink1.XXX”插件版本解压缩，并把整个“NokovLiveLink”文件夹复制，粘贴到UE\_4.26引擎的路径之中，路径在“Epic games\UE\_4.26\Engine\Plugins”。\


    ![17.1.1](<../.gitbook/assets/0 (21).png>)
2.  打开UE引擎创建项目。在UE界面选择“编辑—插件”，将“Animation—Live Link”与“MotionCapture—NokovLiveLink”勾选上（17.1.2、17.1.3），并重启UE使插件生效。\


    ![17.1.2](<../.gitbook/assets/1 (18).png>)

    <figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>
3.  选择“窗口—实时链接”，点击”源—Nokov LiveLink”，ServerIP 和XingYing软件中数据广播面板设置的网卡地址保持一致，默认为10.1.1.198，向上轴（此处和XINGYING保持一致），点击OK。播放XINGYING，接收动捕数据，绿色指示灯亮起（17.1.4）；\


    <figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>
4.  创建动画蓝图，在下方的内容侧滑菜单栏中找到带有“骨骼网格体”的骨骼（17.1.5），右键这个骨骼网格体—创建—动画蓝图（17.1.6），创建好的动画蓝图双击打开。在动画蓝图中右键搜索“实时链接姿势”，并双击打开（17.1.7）；\


    <figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption><p>17.1.5</p></figcaption></figure>



    <figure><img src="../.gitbook/assets/image (35).png" alt="" width="336"><figcaption><p>17.1.6</p></figcaption></figure>



    <figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption><p>17.1.7</p></figcaption></figure>
5.  在“实时链接姿势”的“Live Link Subject Name”中，选择目标Markerset的名称，以该Markerset驱动模型运动，并将“实时链接姿势”与“输出姿势“拖动相连（17.1.8）。并在右侧选择Retarget—Retarget Asset—NokovLiveLinkRetarget Asset（17.1.9）；\


    ![17.1.8](<../.gitbook/assets/7 (13).png>)

    <figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption><p>17.1.9</p></figcaption></figure>
6. 点击编译按钮，UE中的模型就会被驱动，进行同步运动；

![17.1.10](<../.gitbook/assets/9 (9).png>)



![17.1.11](<../.gitbook/assets/10 (8).png>)

{% hint style="info" %}
Live Link窗口打开位置：使用UE\_4.27引擎请选择“窗口->LiveLink”（17.1.10），使用UE\_5.0版本及其后续的UE版本请选择“窗口->虚拟制片->LiveLink”（17.1.11）；
{% endhint %}



***

### **重定向人体数据驱动UE模型**

1. XingYing的人体数据可以通过插件直接接入UE驱动人体模型。但是当模型和模特身体差异较大时，直接驱动模型或出现滑步等情况，此时可以通过MotionBuilder进行绑定和重定向后再通过MotionBuilder的UE插件(MotionBuilder LiveLink，可在UE官网下载或咨询Nokov工程师获取)去驱动UE中的人体模型。你也可以在XingYing中通过导入需要驱动的人体模型，然后开启重定向功能，人体数据经过转换后，输出的数据就可以跳过MB而直接驱动UE中的人体模型。通过XingYing的重定向功能驱动模型，具体操作步骤请详细参考上文中的“十五、数据重定向”；
2.  在XINGYING中将人体骨骼重定向完成后点击解算按钮，骨骼解算完成后在设置中开启“启用重定向数据”，打开UE，将XINGYING中进行了骨骼重定向的模型文件导入UE中，在空白处点击鼠标右键，选择蓝图类（17.1.12），在弹出的窗口的输入框中输入“Nokov”，选择“NokovLiveLinkRetargetAsset”，点击选择（17.1.13），给蓝图类命名，若未重命名，蓝图类默认名称为“NewBlueprint”，此时可以看到内容侧滑菜单中我们成功创建了一个正方体图标的蓝图类；\




    <figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption><p>17.1.12</p></figcaption></figure>



    ![17.1.13](<../.gitbook/assets/12 (8).png>)
3.  双击刚刚创建的蓝图类，可以看到弹出的窗口下方有自适应（Self Adaption）和平移（Use Translation）两个选项，平移选项默认不勾选，自适应默认勾选（17.1.14），保持默认的设置即可，部分少数外部导入的FBX模型需要勾选自适应和平移两个选项，视模型而定；\


    <figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption><p>17.1.14</p></figcaption></figure>
4.  在窗口右侧Retarget—Retarget Asset的下拉框中选择创建的蓝图类（17.1.15），点击编译，XINGYING软件播放，Markerset开始运动，UE中的模型便会被同步驱动起来；\
    \


    <figure><img src="../.gitbook/assets/image (493).png" alt=""><figcaption><p>17.1.15</p></figcaption></figure>
5. 使用骨骼重定向的人体数据驱动UE模型时，若没有勾选或忘记在XINGYING中“启用重定向数据”功能，需要在XINGYING将“启用重定向数据”开启，开启后将UE与XINGYING软件的连接断开，重新进行LiveLink连接，否则会导致人体数据和SDK获取到的描述信息不一致，从而导致UE中模型骨骼异常；



***

### **蓝图类**

1.  双击创建的蓝图类进入（17.1.16）；\


    ![17.1.16](<../.gitbook/assets/15 (8).png>)
2.  Nokov Bone Mapping表中左侧是XINGYING人体的骨骼名称，右侧是UE模型的骨骼名称。在Nokov Bone Mapping选项中选中Enable BoneMapping复选框可编辑下方的列表，不选中则无法编辑，在每段关节骨骼名称的左侧有一个复选框，勾选上，则此段关节骨骼参与数据驱动，不勾选则该骨骼不会参与数据驱动（17.1.17）；\


    ![17.1.17](<../.gitbook/assets/16 (8).png>)
3.  点击单个关节（行）右侧的Select按钮，通过在搜索框中输入骨骼名称，进行模糊匹配目标关节，例如选中“Spine1”这段骨骼，点击Select按钮，在搜索框中输入“Spine”，便可以模糊查询匹配出目标关节了（17.1.18）；\


    ![17.1.18](<../.gitbook/assets/17 (8).png>)
4.  点击窗口底部“Select a skeleton for mapping”，会显示出所有的骨架资源（17.1.19），选中骨架资源来应用这套骨架，检查选择的骨架资源中的骨骼名称是否和XINGYING人体的骨骼名称对应上，若对应错误，可在Select按钮中进行模糊匹配目标关节；\


    ![17.1.19](<../.gitbook/assets/18 (7).png>)
5. 若使用动捕数据驱动UE模型，模型的骨骼显示异常或位置错误，这可能是由于部分模型与XINGYING软件的骨骼名称不一致从而骨骼对应错误，导致在UE中驱动模型后骨骼异常，此时我们需要检查骨骼的名称映射，双击我们创建的蓝图类，在Nokov Bone Mapping列表中检查两侧的骨骼关节是否对应正确，若对应错误，修改后保存点击编译，重新在Retarget—Retarget Asset的下拉框中选择我们刚刚修改的蓝图类名称，点击编译即可成功驱动模型运动；
6.  查看导入UE的模型文件的骨骼名称和骨骼层级，可以双击模型，在模型窗口中点击骨架图标，可以看到窗口右侧树状图显示的就是模型的骨骼名称（17.1.20）；\


    ![17.1.20](<../.gitbook/assets/19 (7).png>)
7. 在骨骼名称树状图中选中模型的一段骨骼，中间的模型便会显示出该骨骼在模型身上的具体位置，通过这种方法来检查UE骨骼名称是否和XINGYING人体骨骼名称对应正确。例如，选中UE模型小臂骨骼，在Nokov Bone Mapping列表中查看UE小臂骨骼名称是否和XINGYING人体的小臂骨骼对应正确，若出现UE小臂骨骼和XINGYING人体的大臂骨骼错误对应了，则需要复制UE模型的小臂骨骼名称，并在Bone Mapping中将复制的小臂骨骼名称与XINGYING人体小臂的骨骼对应，以此类推，检查各段骨骼名称是否一一对应正确，检查完成后，点击保存。XINGYING人体的各个骨骼位置及其骨骼名称可在XINGYING资产面板点击“关节”列表查看；
8. 若将XINGYING骨骼和UE模型的骨骼对应正确后，在UE中驱动模型仍然骨骼显示异常，出现此类情况，请联系我们的技术工程师获取帮助。



***

### **LiveLink刚体运用**

1. 使用UE刚体运用，首先在动作捕捉场地中放入贴好反光标记点的捕捉物，并在实时模式下使用一键创建刚体功能创建一个Markerset。成功创建刚体后，打开软数据广播面板，开启“启用SDK ”；
2. 打开UE工程文件，若首次创建UE工程，请联系我们的技术工程师获取相应的插件版本，并参考上文“插件安装与UE设置”来正确配置我们的插件；
3.  点击UE中的窗口—虚拟制片—LiveLink，在LiveLink窗口中点击添加源，选择“Nokov LiveLink”，IP地址和XINGYING软件保持一致，默认为10.1.1.198，轴向和XINGYING软件轴向保持一致，软件默认Y轴向上（17.1.21）；\


    <figure><img src="../.gitbook/assets/image (494).png" alt=""><figcaption><p>17.1.21</p></figcaption></figure>
4.  在Nokov Server IP的下拉列表中会显示本机所有的网卡地址，也可以点击“Remote Server IP”，在“Nokov Remote IP”输入框中输入IP地址。\


    <figure><img src="../.gitbook/assets/image (495).png" alt=""><figcaption></figcaption></figure>
5.  将各项设置完成后，点击OK，将XIINGYING软件播放，此时可以看到选项卡中绿色指示灯亮起，并显示出所连接上的所有的Markerset名称，角色名称为“变换”代表该Markerset为刚体，若显示的角色名称为“动画”，则表示该Markerset为人体（17.1.22）；\


    <figure><img src="../.gitbook/assets/image (238).png" alt=""><figcaption><p>17.1.22</p></figcaption></figure>
6.  接下来在UE中快速创建一个静态网格体添加到我们的项目中，选择一个几何体（17.1.23）；\


    <figure><img src="../.gitbook/assets/image (496).png" alt=""><figcaption><p>17.1.23</p></figcaption></figure>
7.  创建完后右侧“细节”属性栏中可以看到我们刚才创建的实例，在视图中几何球体已经添加到视图中了，点击添加按钮，输入“LiveLink”，选择“Live Link Controller”组件（17.1.25）；\


    <figure><img src="../.gitbook/assets/image (497).png" alt=""><figcaption><p>17.1.25</p></figcaption></figure>
8.  添加LiveLinkComponentController组件后，选中该组件，在下方的“Subject Representation”的右侧下拉框中选择我们上面LiveLink选项卡中所连接上的刚体名称，点击“Tracker0”（17.1.26），使用名称为“Tracker0”这个刚体来驱动UE中我们添加的几何球体；\


    <figure><img src="../.gitbook/assets/image (498).png" alt=""><figcaption><p>17.1.26</p></figcaption></figure>
9.  选中默认场景的根组件，将组件的移动性改为可移动（17.1.27）；\


    <figure><img src="../.gitbook/assets/image (499).png" alt=""><figcaption><p>17.1.27</p></figcaption></figure>
10. 接下来只需要播放XINGYING软件，让“Tracker0”这个刚体运动起来，UE中几何体便会和刚体做同步运动。



***

### **UE引擎刷新问题解决方法**

*   在UE中使用XINGYING插件驱动模型，XINGYING人体丢失，重新识别上人体后，UE场景中无法显示出模型，该现象是由于UE引擎的刷新问题引起的，若要解决此刷新问题，首先在动画蓝图中将实时链接姿势与输出姿势连线驱动模型后，还需在动画蓝图的事件图表中添加节点，并在添加的各个节点之间连线（17.1.28），这样就可以解决UE引擎不刷新的问题了。\


    <figure><img src="../.gitbook/assets/image (244).png" alt=""><figcaption><p>17.1.28</p></figcaption></figure>
