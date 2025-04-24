# （六）VMarker图表

### 海伦海耶斯人体内置虚拟标记点

1. 在实时下创建的29点、26点、19点海伦海耶斯模型，模板中内置虚拟标记点。
2.  在后处理模式加载海伦海耶斯模型数据后，打开VMarker图表，在资产面板的“虚拟标记”标签页中选中模板的VMarker点，在图表上便会显示出选中的VMarker点的X、Y、Z位置坐标及其最大最小值（11.6.1），3D视图上海伦海耶斯人体关节上的十字Marker便是模板内置的VMarker点。\


    <figure><img src="../.gitbook/assets/image (359).png" alt=""><figcaption><p>11.6.1</p></figcaption></figure>

***

### 创建虚拟标记点

1. 创建虚拟标记点需要模板存在命名点，我们可以在实时模式录制一组带刚体的数据或者在后处理模式手动创建一个刚体，在刚体的各个命名点上绑定虚拟标记点。
2.  首先在资产面板中选中要创建VMarker的刚体模板，然后选中“虚拟标记”标签页，创建虚拟标记点的名称（11.6.2）\


    <figure><img src="../.gitbook/assets/image (360).png" alt=""><figcaption><p>11.6.2</p></figcaption></figure>
3. 在列表中选中VMarker点，在下方的高级属性中设置虚拟标记点的属性（11.6.3）
   * 类型选择默认的“Three-Point（Value）”
   * 虚拟标记点无需设置绑定点
   * 双击“原点、长轴点、平面点”选择命名点，设置完成后，VMarker点初始位置会显示在原点位置
   *   在X、Y、Z偏移输入框中输入偏移值，创建出来的VMarker点的位置会根据偏移值进行偏移，若未设置偏移值，则VMarker点会显示在原点位置\


       <figure><img src="../.gitbook/assets/image (361).png" alt=""><figcaption><p>11.6.3</p></figcaption></figure>
4. 依次按照上述操作对创建的其他虚拟标记点设置属性，在资产列表中点击保存按钮来保存此次创建的虚拟标记点。
5.  打开VMarker图表，选中我们创建的虚拟标记点，在图表上便会显示出该虚拟标记点的波形及其XYZ坐标和最大最小值。\


    <figure><img src="../.gitbook/assets/image (363).png" alt=""><figcaption><p>11.6.4</p></figcaption></figure>
6. 点击左上角的文件--保存动捕数据。切换到实时模式后加载带虚拟标记点的刚体资产，点击播放，刚体识别后，在3D视图上便会显示出虚拟标记点。

