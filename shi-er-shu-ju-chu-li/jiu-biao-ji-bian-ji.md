# （九）标记编辑

新增标记编辑菜单（12.9.1），用于后处理模式下，错误数据的查找和修复。

<figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption><p>12.9.1</p></figcaption></figure>

* **移除坏数据**

输入加速度阈值，查询当前数据中的错误帧，并在分析图表（12.9.2）、健康视图（12.9.3）中显示出有问题的帧。查询出错误数据后，可以点击剪切按钮，将问题的帧删除。

<figure><img src="../.gitbook/assets/image (65).png" alt=""><figcaption><p>12.9.2</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (66).png" alt=""><figcaption><p>12.9.3</p></figcaption></figure>

* **查找间隙**

选择资产和标记点后，点击查找上一个、查找下一个按钮，会查询该标记点的数据中缺帧的数据段并在分析图表（12.9.4）、健康视图（12.9.5）中显示出来。

<figure><img src="../.gitbook/assets/image (68).png" alt=""><figcaption><p>12.9.4</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (67).png" alt=""><figcaption><p>12.9.5</p></figcaption></figure>

* **填充间隙**

在通过以上的步骤查找到有问题的数据帧或者帧范围时，可以选择使用以下几种方法对有问题的数据进行修复。

<figure><img src="../.gitbook/assets/image (63).png" alt=""><figcaption><p>12.9.6</p></figcaption></figure>

1、使用插值填充

插值填充方式：线性连接、三次方连接。

待修复的帧范围：当前帧、选中范围帧、所有帧。

最大间隙长度：在此范围内的丢帧才进行修复，否则不进行任何操作。

填充所有标记：勾选时对当前资产的所有Marker都进行修复，否则只修复手动选中的Marker。



2、使用刚性填充

待修复的帧范围：当前帧、选中范围帧、所有帧。

参考标记点：修复数据时，参考刚性结构中未丢失的点数据，在点击“选择参考标记”按钮后，在3D视图中，用鼠标点击作为参考的标记点（必须选择3个）。

<figure><img src="../.gitbook/assets/image (60).png" alt=""><figcaption><p>12.9.7</p></figcaption></figure>

3、使用约束填充

待修复的帧范围：当前帧、选中范围帧、所有帧。



4、复制轨迹

待修复的帧范围：当前帧、选中范围帧、所有帧。

复制标记点：修复数据时，复制资产中另一个未丢帧Marker点的数据轨迹，在点击“选择复制标记”按钮后，在3D视图中，用鼠标点击作为参考的标记点（只能选择1个）。



* **数据平滑**

1、多点平滑

可选择”3 点平滑、5 点平滑、7 点平滑“，可对 Marker 点数据进行平滑

2、巴特沃斯平滑

设置截止频率（范围1\~30HZ）、出入平滑参数，点击应用，可对Marker 点数据进行平滑

3、撤销

在对Marker数据进行平滑后，如果对效果不满意，可以点击工具栏的“撤销”按钮进行回退。

<figure><img src="../.gitbook/assets/image (64).png" alt=""><figcaption><p>12.9.8</p></figcaption></figure>
