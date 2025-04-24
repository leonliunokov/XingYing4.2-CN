# （五）Maya插件

### **插件安装**

1. 下载最新的插件版本：Nokov-MayaPlugin XXX(2018-2022).exe；
2.  插件安装包解压缩，双击解压缩后的插件，把插件安装在软件目录之中，（17.5.1）。完成之后，点击Next--Install，等待插件安装完成（手套人体在Maya中的应用同下）；\


    <figure><img src="../.gitbook/assets/image (506).png" alt="" width="545"><figcaption><p>17.5.1</p></figcaption></figure>



***

### **Maya的设置与使用**

1.  点击“窗口—设置/首选项—插件管理器”，在其中搜索“Plugin”，并勾选“PluginMaya.mll”的两个窗口（17.5.2）。鼠标放在图标上可看到详细信息；\


    <figure><img src="../.gitbook/assets/image (276).png" alt=""><figcaption><p>17.5.2</p></figcaption></figure>
2.  关闭插件管理器，在Maya下方MLE窗口搜索“NokovPluginWindow”，按下回车键调出插件窗口；\


    <figure><img src="../.gitbook/assets/image (474).png" alt=""><figcaption></figcaption></figure>
3.  选择与XINGYING软件一致的网卡地址，点击Offline，使其到Online状态。勾选RefreshUI，将动捕软件播放后Maya开始持续接受来自动捕的数据；\


    <figure><img src="../.gitbook/assets/image (475).png" alt=""><figcaption></figcaption></figure>
4.  XINGYING软件里的人体运动起来后，Maya中的模型就会被驱动，进行同步运动。\


    <figure><img src="../.gitbook/assets/image (476).png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
注意：由于Maya的骨骼节点不允许数字名称，所以在XINGYING软件的人体Markerset名称不能以数字开头或者纯数字，否则会导致Maya中显示不出骨架；
{% endhint %}



***

### **角色化**

1.  在Maya中手动创建动捕人体数据的角色化，Maya获取到人体数据后在插件窗口中点击“Characterize”按钮，点击右上角“切换角色控制”选项，再点击“创建角色定义”；\


    <figure><img src="../.gitbook/assets/image (477).png" alt=""><figcaption></figcaption></figure>



    <figure><img src="../.gitbook/assets/image (478).png" alt="" width="241"><figcaption></figcaption></figure>
2.  对角色的每个骨骼进行“Assign Selected Bone”操作，骨骼全部绑定完成后，角色化成功；\


    <figure><img src="../.gitbook/assets/image (479).png" alt=""><figcaption></figcaption></figure>
3.  导入想要驱动的模型到Maya中，重复上述步骤给导入的模型创建角色化。创建完成后角色栏选择导入的模型角色，源栏选择XINGYING人体骨骼角色，以实现骨骼与模型的绑定，播放后模型会被驱动起来。\


    <figure><img src="../.gitbook/assets/image (480).png" alt=""><figcaption></figcaption></figure>



***

### 未命名点的显示

*   在NokovPluginWindow窗口中勾选“UnnamedMarkers”复选框，在Maya场景中便会显示出未命名点。\


    <figure><img src="../.gitbook/assets/image (481).png" alt=""><figcaption></figcaption></figure>

***

### Characterize按钮

* 获取到人体数据后，点击插件窗口中的“Characterize”按钮，在场景中会强制将人体的姿势变为标准的T-Pose姿势。

### Lock按钮

* 点击插件窗口中的“Characterize”按钮后，数据会停留在当前这一帧，点击Lock按钮解锁后，即可继续接收到来自XINGYING软件的人体数据
* XINGYING人体骨架需要和导入模型的骨架姿势保持一致，所以在角色化前可以先点击“Characterize”按钮将人体骨架强制变为T-Pose姿势，再进行XINGYING人体数据和导入的模型的角色定义（建议导入标准T-Pose姿势的模型），选择正确的角色和源后再点击Lock按钮解锁，这样XINGYING人体骨架和模型在运动时的姿势会保持一致。

***

### ServerIP

*   打开NokovPluginWindow插件窗口后，点击ServerIP，可展开IP选择的下拉框，在下拉框中会显示当前主机的全部IP地址（17.5.11），选择与XINGYING广播地址同一网段的IP地址即可，默认选择“10.1.1.198”。也可以选择下拉框中的“input the remote ip”，在下方的“Remote”输入框中手动输入IP地址勾选Online复选框连接动捕数据。\


    <figure><img src="../.gitbook/assets/image (507).png" alt=""><figcaption></figcaption></figure>
