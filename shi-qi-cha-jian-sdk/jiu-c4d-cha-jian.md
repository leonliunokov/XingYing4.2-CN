# （九）C4D插件

### 插件安装与准备

#### 1、安装Nokov\_C4D\_Plugin <a href="#toc30470" id="toc30470"></a>

下载插件，运行Nokov\_C4D\_Plugin安装程序，安装路径选择C4D软件的根目录，例如（C:\Program Files\Maxon Cinema 4D 2023）。

<figure><img src="../.gitbook/assets/image (129).png" alt="" width="556"><figcaption><p>9.1</p></figcaption></figure>

#### 2、XingYing软件准备 <a href="#toc17214" id="toc17214"></a>

打开形影软件，在实时模式下捕捉人体或播放后处理人体数据，并勾选SDK,发送数据。

&#x20;

### &#x20;功能介绍与使用

#### 1、配置IP与连接形影软件 <a href="#toc11013" id="toc11013"></a>

打开C4D软件，点击顶部的拓展按钮，找到Nokov Mocap Live并点击打开插件面板(9.2)。



<figure><img src="../.gitbook/assets/image (130).png" alt="" width="493"><figcaption><p>9.2</p></figcaption></figure>

#### 2、配置IP与连接形影软件 <a href="#toc11013" id="toc11013"></a>

配置IP与形影中SDK发送数据的IP一致，点击连接按钮(9.3)。

<figure><img src="../.gitbook/assets/image (131).png" alt="" width="401"><figcaption><p>9.3</p></figcaption></figure>

#### 3、创建人体骨骼并驱动 <a href="#toc18693" id="toc18693"></a>

连接成功后点击Create Skeleton按钮创建人体骨骼(9.3)，选中创建出来的人体骨骼，在右侧的对象列表中找到刚刚选中的人体骨骼并点击Hips骨骼后面的Nokov标签(9.4)，展开标签属性中的Character，将Name改为需要使用的形影中的人体的名字，按下回车，然后点击界面下方的播放按钮即可驱动。

<figure><img src="../.gitbook/assets/image (127).png" alt="" width="504"><figcaption><p>9.4</p></figcaption></figure>

#### 4、手动设置标签属性 <a href="#toc2299" id="toc2299"></a>

如果Nokov标签被删除，可以选中骨骼的Hips后点击右上角的标签->拓展->PluginC4D标签->NokovMocapLive，或直接在Hips上点击右键拓展->PluginC4D标签->NokovMocapLive重新添加标签(9.5)。

<figure><img src="../.gitbook/assets/image (125).png" alt=""><figcaption><p>9.5</p></figcaption></figure>

重新添加标签后需要手动配置便签属性，点击刚刚添加的nokov标签，展开标签属性中的Character，将Name改为需要使用的形影中的人体的名字(9.4)。然后展开Joints Controler，选中Hips后点击Detect Joints Map按钮一键绑定骨骼映射关系(9.4)，也可以手动拖拽场景元素到对应的位置，或者点击画笔按钮选取元素(9.6)。

<figure><img src="../.gitbook/assets/image (128).png" alt=""><figcaption><p>9.6</p></figcaption></figure>

#### 5、其他功能 <a href="#toc22634" id="toc22634"></a>

骨骼映射关系后面的复选框R和P，分别决定是否使用动捕数据的旋转数据和位移数据。

Clear Joints Map按钮，点击可以一键清除当前标签中设置的所有骨骼映射关系。

Set T-Pose，将当前标签中绑定好映射关系的骨骼的姿势设置为TPose姿势。

Go To T-Pose，使当前绑定好的将当前标签中绑定好映射关系的骨骼呈现为Set T-Pose按钮设置的T-Pose姿势，仅在使用Set T-Pose设置过T-Pose姿势后才会起作用。在连接成功且name设置为形影中人体的名称时，姿势会被覆盖，也会不起作用。

Scale Root Position，勾选后将根据形影数据和骨骼的比例差异缩放形影数据，仅在使用Set T-Pose设置过T-Pose姿势后且勾选了复选框“P”后才会生效。

<figure><img src="../.gitbook/assets/image (120).png" alt=""><figcaption><p>9.7</p></figcaption></figure>

插件面板上的Begin Record按钮和End Record按钮(9.8)，在接收到动捕数据驱动人体骨骼后，可以点击Begin Record按钮开始录制数据，点击End Record按钮结束录制，录制的最大时间需要在C4D底部设置最大帧数设置(9.9)，默认30帧为一秒。

<figure><img src="../.gitbook/assets/image (121).png" alt="" width="361"><figcaption><p>9.8</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (122).png" alt=""><figcaption><p>9.9</p></figcaption></figure>
