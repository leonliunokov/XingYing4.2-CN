---
description: 目前已经对接的放大器型号为5695B，测力台型号为9260AA6和9287CA。
---

# Kistler

1. 环境准备，安装BioWare5.3.2.9软件，安装64位DataServer。Win11上安装需要安装64位Instacal。
2.  插上测力台USB线，打开BIOWare软件，首次启动会提示检测到USB设备，需要配置；\


    <figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>
3. 点击ok按钮;
4.  如果测力台是首次使用，需要点击如下图中红框的图标进行测力台校准。在弹出的对话框中根据提示进行操作即可\


    <figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>
5.  依次点击setup->Hardware->devices 然后选择New;\


    <figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>
6.  根据测力台的模拟通道数选择对应通道。这里我们使用的测力台是8通道的。选择8CHannel，点击下一页 。\


    <figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>
7.  在Enter DEvices type下拉选择对应的测力台型号。这里我们选择了9260AA5，然后输入一个名称，这里名称可以任意指定，主要用于多测力台排序使用。最后填上测力台正确的序列号信息，点击下一步。\


    <figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>
8.  正常情况下测力台尺寸参数这块不用修改，直接点击下一步。\


    <figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>


9.  接下来需要填入正确的测力台参数矩阵，这个矩阵信息是跟随测力台一起发货的，如果遗失，需要找对应代理商申请原始信息。\


    <figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>


10. 这个矩阵信息很重要，一定确保不能填错。另外需要注意阵单位是mV。
11. 点击下一步，然后将设备加入active devices 的列表中。在弹出的启示通道选择通道1.，如果有多个测力台，则第二个测力台的起始通道为8，以此类推
12. 设备配置完成后，点击setup ->save dataServer Configuration File，将当前的设备配置信息保存到本地电脑，格式为xml格式。
13. 打开xingying。选择第三方设备->测力台配置，在测力台一栏点击“+”增加一个测力台，点击测力台名称，在右侧的设备列表下拉选择Kistler。
14. 在其它配置栏勾选kistler测力台（数字），在弹出的对话框中点击选择文件，选择刚才保存的xml文件。
15. 点击确定，关闭对话框，接下来就可以使用测力台了。

