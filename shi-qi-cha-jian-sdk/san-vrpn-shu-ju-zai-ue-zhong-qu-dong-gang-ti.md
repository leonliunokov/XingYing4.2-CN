# （三）VRPN数据在UE中驱动刚体

1. 使用VRPN将刚体数据传到UE，在UE场景中通过动捕软件的刚体来驱动物体，首先在XINGYING中将“VRPN”功能开启，将捕捉物贴好反光标记点，在实时模式下创建刚体，确保软件处于播放状态；
2. 打开XINGYING设置界面，由于UE的VRPN对接收数据时会以m为单位进行处理，所以在动捕中将数据单位修改为meter。
3.  打开UE软件，点击左上方的“编辑→插件”打开插件设置窗口，在搜索框输入“VRPN”、“Live”，分别将“LiveLinkVRPN”和“LiveLink”勾选上，重启UE软件（17.3.1）；\


    <figure><img src="../.gitbook/assets/image (259).png" alt=""><figcaption><p>17.3.1</p></figcaption></figure>
4.  点击“窗口→LiveLink”，在“LiveLink”窗口中添加“LiveLinkVRPN源”，在“Connection Settings”中，“IPAddress”请保持默认不要修改，“Local Updata Rate in Hz”中的帧率与VR Tracker软件设置的帧率保持一致，“Device”输入在VR Tracker中创建的刚体名称，“Subjectname”表示主题命名，“Type”选择“Tracker”（17.3.2），点击添加，刚体的主题就会被添加进来。\


    <figure><img src="../.gitbook/assets/image (260).png" alt=""><figcaption><p>17.3.2</p></figcaption></figure>
5.  选中刚体的主题，点击“前处理器”右侧的“+”，在下拉框中选择“变换轴切换”，在“变换轴切换”的下拉框中，修改“前向轴、右向轴、向上轴”（17.3.3）使UE中的变换轴和VR Tracker软件中标定的坐标系轴向一致。以VR Tracker软件Y轴向上为例，可以看到当坐标系为Y轴向上时，前向轴为X、右向轴为Z、向上轴为Y，那么在UE中也将前向轴、右向轴、向上轴分别设置为“X、Z、Y”；\


    <figure><img src="../.gitbook/assets/image (261).png" alt=""><figcaption><p>17.3.3</p></figcaption></figure>
6. 接下来的操作参考上文“十七、插件\&SDK （一）UE插件 LiveLink刚体应用”的步骤5\~9。
