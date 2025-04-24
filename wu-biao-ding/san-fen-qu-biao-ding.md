# （三）分区标定

1.  设备列表新增“区域设置”菜单，可以对已连接的镜头进行区域划分（5.3.1）。\


    <figure><img src="../.gitbook/assets/image (49).png" alt="" width="289"><figcaption><p>5.3.1</p></figcaption></figure>

    <figure><img src="../.gitbook/assets/image (52).png" alt="" width="563"><figcaption><p>5.3.2</p></figcaption></figure>
2. 根据场地的实际布局，将镜头添加到不同的区域（5.3.2）。
3. 分区域进行L+T标定，在标定区域1时，只使能区域1的镜头，对其他区域的镜头进行不使能。标定完成后另存标定文件为setup-area1.cal。
4. 重复以上的步骤，按顺序对所有的区域进行标定，保存各个区域的标定文件，待下一步合并标定时使用。
5.  待所有区域都标定完成后，打开标定-设置-区域合并页面（5.3.3），分别选择区域1和区域2的标定文件，设置XYZ偏移的参数，点击合并。\


    <figure><img src="../.gitbook/assets/image (59).png" alt="" width="289"><figcaption><p>5.3.3</p></figcaption></figure>


6. 对合并完成的场地进行更新标定，更新标定完成后，即可以正常进行捕捉。\

7. 如果存在3个及3个以上的区域时，先完成区域1和区域2的合并，然后将合并完的区域作为区域1和区域3进行再次合并，依次类推，完成所有区域的合并。

{% hint style="info" %}
XYZ偏移的测量方法：

1、确定场地1为主场地，场地2为待合并场地

2、测量坐标偏移量

3、以场地1的L型杆为坐标轴原点，测量场地2的L型杆和场地1的L型杆的距离
{% endhint %}

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>





