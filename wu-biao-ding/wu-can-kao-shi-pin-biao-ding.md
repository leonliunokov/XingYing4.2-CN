# （五）参考视频标定

### **参考视频标定**

1. XINGYING支持接入普通工业相机或高速工业相机，首先将工业相机的USB线连接电脑；
2.  打开XINGYING软件，连接相机并播放。将T型杆放入捕捉场景中，并快速创建一个刚体；在软件上方工具栏点击“视频标定”面板，也可在视图菜单栏中选择“视频标定”打开，打开参考视频。\


    <figure><img src="../.gitbook/assets/image (460).png" alt=""><figcaption></figcaption></figure>
3. 按照视频标定面板下方的提示步骤标定，将T型杆放在参考视频可见的范围内，点击“开始标定”；
4.  确定T型杆的位置后点击冻结帧，对照资产面板中Marker名称的ID在参考视频中按顺序在参考视频中点击T型杆上对应的marker球。\


    <figure><img src="../.gitbook/assets/image (461).png" alt=""><figcaption></figcaption></figure>
5.  选取T型杆上的marker球后参考视频中点击的位置会绘制白色标记，标定数据中也会显示选取的点的坐标，接下来点击添加帧按钮，会将当前这一帧的标定数据添加进去，上方显示的“添加帧数”会变为1。

    <figure><img src="../.gitbook/assets/image (462).png" alt=""><figcaption></figcaption></figure>
6. 将T形杆换个位置重复步骤4\~5的操作（6次及其以上直到出现“完成标定”按钮出现）。确保在空间中的左上角、左下角、右上角、右下角、中间、前后这几个位置采集到标定的数据。这样标定后在参考视频上叠加显示的内容会更加准确；
7.  当出现完成标定按钮时，点击“完成标定”，界面会弹出一个标定文件保存窗口，输入文件名称点击保存；\


    <figure><img src="../.gitbook/assets/image (463).png" alt=""><figcaption></figcaption></figure>

***

### **参考视频叠加**

1.  参考视频标定完成后参考视频中会叠加显示3D视图中的内容，如命名点、Link连线、骨骼、未命名点，人体模板和刚体模板也可以在参考视频 上叠加显示。\


    <figure><img src="../.gitbook/assets/image (464).png" alt=""><figcaption></figcaption></figure>
2.  若需要关闭叠加显示，可以在3D视图中的右键菜单中进行关闭。例如在右键菜单中将骨骼显示关闭，3D视图上将不会显示模板的骨骼，参考视频中也不会叠加显示骨骼。\


    <figure><img src="../.gitbook/assets/image (465).png" alt=""><figcaption></figcaption></figure>


3. 在参考视频上也可以叠加显示内置皮肤，例如在创建53点类型的人体模型后，在资产面板的属性选项中选择内置的人体皮肤“NokovMale.fbx”，参考视频中也会叠加显示人体皮肤。



