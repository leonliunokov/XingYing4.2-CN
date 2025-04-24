# （八）TimeCode时间码在UE中的应用

### **插件安装与软件设置**

1. 以UE5.0版本为例介绍TimeCode的应用。将UE插件拷贝到“\UE\_5.0\Engine\Plugins”目录下，插件版本请咨询技术工程师获取；
2.  新建一个UE工程，打开UE软件，在编辑中打开插件设置，在搜索框中搜索MotionCapture，将“NokovLiveLink”插件勾选上，搜索“Virtual Production”，勾选上“Virtual Production Utilities”（17.8.1），上述两个选项全部勾选上后，将UE重启。\


    <figure><img src="../.gitbook/assets/image (314).png" alt=""><figcaption><p>17.8.1</p></figcaption></figure>
3.  在XINGYING软件中将软件播放，将未命名点快速创建一个刚体，在软件上方工具栏打开数据广播面板，TimeCode模块下勾选“启用”复选框（如17.8.2），右侧的端口号和帧率请勿修改，保持默认的5850端口和24Fps即可。\


    <figure><img src="../.gitbook/assets/image (315).png" alt=""><figcaption><p>17.8.2</p></figcaption></figure>
4. 开启TimeCode后将XINGYING软件播放，在3D视图左下方会显示出TimeCode字段，字段的含义分别为：时、分、秒、帧、子帧，子帧号的跳动代表TimeCode帧率和软件设置帧率的两个帧率之间的比例；



***

### **LiveLink连接与设置**

1. 确保XINGYING软件已经开启SDK广播，广播地址默认10.1.1.198，在UE中点击“窗口—虚拟制片—LiveLink”，在LiveLink窗口中点击源，选择Nokov LiveLink，点击OK，可以看到已经连接上数据源了；
2. 点击“窗口—虚拟制片—时间码提供方”，在“时间码提供方”窗口中显示的时间码默认和电脑系统的时间是一致的；
3.  在LiveLink窗口下方的主题列表中选中“NokovLiveLink”，勾选“TimeCode Provider”替换为数据源的TimeCode时间码，展开LiveLink窗口右侧的“帧率”，将FPS设置为和XINGYING软件同样的帧率，保持一致（17.8.3）。\


    <figure><img src="../.gitbook/assets/image (316).png" alt=""><figcaption><p>17.8.3</p></figcaption></figure>



***

### **UE与XINGYING时间码同步**

1. 打开“时间码提供方”窗口，显示的时间码会和数据源一致，也就是和XINGYING软件TimeCode时间码保持一致；
2.  点击“窗口—过场动画—镜头试拍录制器”，在录制器窗口中显示的时间码是和XINGYING软件中的时间码是同步的（17.8.4），前提是需要在LiveLink窗口中连接上数据源并勾选“TimeCode Provider”复选框。在使用录制器录制数据时，会把XINGYING软件中的时间码记录下来；\


    <figure><img src="../.gitbook/assets/image (317).png" alt=""><figcaption><p>17.8.4</p></figcaption></figure>



***

### **命名点创建**

1.  点击LiveLink窗口的数据源，在右侧勾选“Create Labeled Marker Subjects”选项来创建命名点，创建成功后左侧主题列表中会自动创建一个“Markers\_xxx”的主题名称（17.8.5）；\


    <figure><img src="../.gitbook/assets/image (318).png" alt=""><figcaption><p>17.8.5</p></figcaption></figure>
2.  选中创建的命名点主题名称，在窗口右上角的“视图选项”下拉中选择“显示静态数据”，将“骨骼命名”展开，会列举出当前Markerset的所有命名点的名称（17.8.6）；\


    <figure><img src="../.gitbook/assets/image (319).png" alt=""><figcaption><p>17.8.6</p></figcaption></figure>
3.  在“视图选项”下拉中选择“显示帧数据”，展开“骨架—变换—索引”，可以实时看到每一个命名点的位置坐标数据，展开“场景时间”，可以实时观测到帧数、时间码、时间码帧率（17.8.7）；\


    <figure><img src="../.gitbook/assets/image (320).png" alt=""><figcaption><p>17.8.7</p></figcaption></figure>



***

### **未命名点创建**

1.  点击LiveLink窗口的数据源，在右侧勾选“Create Unlabeled Marker Subjects”选项来创建命名点，创建成功后左侧主题列表中会自动创建一个“Markers\_Unlabeled”的主题名称（17.8.8）；\


    <figure><img src="../.gitbook/assets/image (321).png" alt=""><figcaption><p>17.8.8</p></figcaption></figure>
2. 创建未命名点后，会自动创建一百个未命名点名称，可以在“视图选项—显示静态数据—骨架—骨骼命名”中看到；展开“视图类型—显示帧数据—骨架—变换—索引”，会显示出未命名点的位置坐标数据，若XINGYING软件中无未命名点，则此处未命名点的值为0，当XINGYING软件中出现了未命名点时，此处未命名点的值才会被填充上位置坐标数据。
