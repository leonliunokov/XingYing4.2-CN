# （四）数据修复

1.  点击上方工具栏“二分屏（上/下）”按钮，让主界面分割为上下两个窗口，选中窗口时会有黄色边框，此时在窗口左上方的下拉菜单中，让其中一个窗口显示“3D视图”，一个窗口选择“分析图表”（12.4.1）；\


    <figure><img src="../.gitbook/assets/image (522).png" alt=""><figcaption></figcaption></figure>
2.  在资产面板或在左侧分析图表资产面板选择Marker点，即可在窗口中看到该反光标记点的 XYZ 坐标曲线（12.4.2）；\


    <figure><img src="../.gitbook/assets/image (523).png" alt=""><figcaption></figcaption></figure>
3. 可以使用键盘上下键的快捷键在资产面板中选择Marker名称；若想一次性全选“Marker名称”，可以使用“Ctrl+A”的组合键来全选上marker名称；

#### &#x20;**修复丢点数据** <a href="#toc31333" id="toc31333"></a>

1.  检查Markerset的每个 Marker 点，看数据是否有丢失，当数据帧上Marker点有丢失时，图表中会显示出数据丢失标识（12.4.3），这可以帮助我们快速定位到丢点帧，数据丢失后通过摁住鼠标中键在时间轴上进行拖动，将有丢失数据的部分包含在内，点击工具栏中的“三次方连接”按钮进行修补，注意当丢失的数据波动较大、有连续五帧丢失时，我们不建议使用三次方连接进行修补；\


    <figure><img src="../.gitbook/assets/image (524).png" alt=""><figcaption></figcaption></figure>

#### **修复未识别的Marker点** <a href="#toc31333" id="toc31333"></a>

1. 在软件暂停的状态下缓慢拖动数据进度条，观察3D视图中模型是否有未识别上的Marker点，若在某一帧上存在未识别上的Marker点，点击逐帧播放按钮对数据进行逐帧播放，确定是从哪一帧开始丢点的，确定该点的名称（在资产面板查看Marker名称）。
2.  **单帧不识别**：点击quick id按钮，弹出对话框，在资产面板中选中未识别上的Marker点的名称后，quick id对话框中点的名称也会变成属性栏中选中的点的名称（12.4.4），在3D视图中点击未识别上的Marker点，此时该Marker点就已经识别正确，由白色的未命名点变为彩色的命名点了，Marker点之间的Link连线也会自动补齐。\


    <figure><img src="../.gitbook/assets/image (525).png" alt=""><figcaption></figcaption></figure>
3. **多帧未识别**：若某一个Marker点在一段连续帧上均未识别上或未识别正确，将这段异常的连续帧包含在选择范围内，打开quick id对话框，在资产面板中选中要修复的Marker点的名称对3D视图上的点进行识别，点击跟踪识别按钮，修复的点在选择范围中会被正确识别上。
4.  若使用quick id功能去固定识别修复一个点的情况下，可以将quick id值锁定（12.4.5），这样快速识别后quick id对话框中的Marker点名称就不会自动增加了，方便操作。\


    <figure><img src="../.gitbook/assets/image (97).png" alt=""><figcaption><p>12.4.5</p></figcaption></figure>
5. 数据修复完成后在资产面板中点击保存按钮，点击“文件 – 保存动捕数据”。
