# Alkeria

### **安装高速工业相机驱动**

1.  下面以Alkeria高速工业相机为例：使用Alkeria高速工业相机需要安装相机的驱动，打开驱动安装包，双击“SDK-MaestroUSB3\_Windows-v2.8.0.exe”来安装驱动（16.3.2.1），在安装过程中选择默认安装路径点击“Next”，选择“I agree”，点击“Install”等待安装完成即可。\


    <figure><img src="../../.gitbook/assets/image (174).png" alt=""><figcaption><p>16.3.2.1</p></figcaption></figure>
2. 成功安装驱动后，电脑桌面会生成一个“MaestroUSB3”的工具（16.3.2.2），双击“MaestroUSB3”，在弹出的文件夹中进入Bin— .NET x64路径中（16.3.2.3），将高速工业相机的USB线插在电脑的USB3.0的口上，双击“AlkeriaPlayer64.exe”进入相机播放器界面（16.3.2.4）。

<figure><img src="../../.gitbook/assets/image (175).png" alt=""><figcaption><p>16.3.2.2</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (176).png" alt=""><figcaption><p>116.3.2.3</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (177).png" alt=""><figcaption><p>16.3.2.4</p></figcaption></figure>





***

### **连接配置高速工业相机**

1.  电脑接入Alkeria高速工业相机后，在工业相机播放器中点击播放按钮后（16.3.2.5），播放器窗口的中间便会显示出相机的图像画面，若点击播放按钮后弹窗报错，请点击“Init Camera”按钮对相机进行初始化（16.3.2.6），初始化后点击播放便可显示出相机的图像画面了。\


    <figure><img src="../../.gitbook/assets/image (178).png" alt=""><figcaption><p>16.3.2.5</p></figcaption></figure>



    <figure><img src="../../.gitbook/assets/image (179).png" alt=""><figcaption><p>16.3.2.6</p></figcaption></figure>
2.  在播放器中播放相机的图像画面后，用户可以根据自己的需求来配置相机的各项参数。点击“Settings”按钮调出设置菜单（16.3.2.7），可在设置菜单中修改相机的亮度、曝光等参数（16.3.2.8），根据个人的需求来进行配置。若将相机参数配置好后，重新拔插高速工业相机的USB线会导致设置中配置的参数恢复默认值，需要在“Settings”中重新配置相机参数。 \


    <figure><img src="../../.gitbook/assets/image (180).png" alt=""><figcaption><p>16.3.2.7</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (181).png" alt=""><figcaption><p>16.3.2.8</p></figcaption></figure>



***

### **Alkeria高速工业相机与动捕的同步**

1. 安装XINGYING 3.1.1.X版本，以管理员运行XINGYING，正确标定。
2. 标定完成后，对Alkeria高速工业相机进行参考视频标定，标定完成后即可实现同步（详细步骤请参考上文“十六、第三方适配 （八）参考视频的标定”）

{% hint style="warning" %}
注意事项：使用Alkeria高速工业相机时，相机播放器和XINGYING的参考视频只能播放一个，不能同时播放，在XINGYING软件中使用参考视频视图播放高速工业相机图像时，请将播放器断开播放（16.3.2.9）。
{% endhint %}

<figure><img src="../../.gitbook/assets/image (182).png" alt=""><figcaption><p>16.3.2.9</p></figcaption></figure>



***

### **录制参考视频**

1. 工业相机的参考视频标定成功后，我们可以录制3D视图与工业相机同步的数据，将界面切换为3D视图和参考视频双视图，输入录制文件名称并勾选“参考视频”选项，点击录制按钮进行录制。
2.  录制完成后在后处理模式将界面切换为3D视图和参考视频双视图，加载录制的数据，点击播放就可以看到参考视频和3D视图同步的效果了（16.3.2.10）。\


    <figure><img src="../../.gitbook/assets/image (183).png" alt=""><figcaption><p>16.3.2.10</p></figcaption></figure>
