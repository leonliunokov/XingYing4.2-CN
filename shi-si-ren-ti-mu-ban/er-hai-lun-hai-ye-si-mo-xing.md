# （二）海伦海耶斯模型

### **Helenhayes贴点说明**

<table data-header-hidden><thead><tr><th width="159"></th><th width="133"></th><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td>描述</td><td>Marker点名称</td><td>Helenhayes FullBodyWithHead(29 Static)</td><td>Helenhayes FullBody(26 Static)</td><td>Helenhayes LowerBody(19 Static)</td><td>放置位置</td></tr><tr><td>头顶</td><td>Top.Head</td><td>√</td><td></td><td></td><td>在头顶的中央顶部</td></tr><tr><td><p>头的前面</p><p>头的后面</p></td><td><p>Front.Head</p><p>Rear.Head</p></td><td>√</td><td></td><td></td><td>在头的前部和后部</td></tr><tr><td><p>左肩</p><p>右肩</p></td><td><p>L.Shoulder</p><p>R.Shoulder</p></td><td>√</td><td>√</td><td></td><td>肩峰突起的尖端</td></tr><tr><td><p>左肘</p><p>右肘</p></td><td><p>L.Elbow</p><p>R.Elbow</p></td><td>√</td><td>√</td><td></td><td>肱骨外上髁</td></tr><tr><td><p>左手腕</p><p>右手腕</p></td><td><p>L.Wrist</p><p>R.Wrist</p></td><td>√</td><td>√</td><td></td><td>在桡骨茎突和尺骨茎突中间</td></tr><tr><td>骶骨</td><td>R.Offset</td><td>√</td><td>√</td><td></td><td>骶骨接口处的上位面</td></tr><tr><td><p>左前腰</p><p>右前腰</p></td><td><p>L.ASIS</p><p>R.ASIS</p></td><td>√</td><td>√</td><td>√</td><td>盆骨前部左右两侧突出的骨头上</td></tr><tr><td><p>左大腿上部</p><p>右大腿上部</p></td><td><p>L.Thigh</p><p>R.Thigh</p></td><td>√</td><td>√</td><td>√</td><td>大腿中部往上1cm</td></tr><tr><td><p>左外侧膝</p><p>右外侧膝</p></td><td><p>L.Knee</p><p>R.Knee</p></td><td>√</td><td>√</td><td>√</td><td>将标记放在膝关节轴的外侧突出处</td></tr><tr><td><p>左内侧膝</p><p>右内侧膝</p></td><td><p>L.Knee.Medial</p><p>R.Knee.Medial</p></td><td>√</td><td>√</td><td>√</td><td>膝关节轴的内侧突出处</td></tr><tr><td><p>左外侧踝关节</p><p>右外侧踝关节</p></td><td><p>L.Ankle</p><p>R.Ankle</p></td><td>√</td><td>√</td><td>√</td><td>踝轴的侧面，内踝骨的外侧突出处</td></tr><tr><td><p>左内侧踝关节</p><p>右内侧踝关节</p></td><td><p>L.Ankle.Medial</p><p>R.Ankle.Medial</p></td><td>√</td><td>√</td><td>√</td><td>踝轴的内侧;内踝骨的内侧突出处</td></tr><tr><td><p>左脚趾</p><p>右脚趾</p></td><td><p>L.Toe</p><p>R.Toe</p></td><td>√</td><td>√</td><td>√</td><td>脚的中心，在第二和第三跖骨中间</td></tr><tr><td><p>左脚跟</p><p>右脚跟</p></td><td><p>L.Heel</p><p>R.Heel</p></td><td>√</td><td>√</td><td>√</td><td>脚跟骨中心</td></tr></tbody></table>



***

### **Helenhayes骨骼说明**

<table data-header-hidden><thead><tr><th width="169"></th><th width="163"></th><th></th><th></th><th></th></tr></thead><tbody><tr><td>骨骼名称</td><td>Origin Marker</td><td>Long Axis</td><td>Plane Axis</td><td>父段骨骼</td></tr><tr><td>Pelvis</td><td>V_Pelvis_Origin</td><td>V_Mid_Hip</td><td>V.Sacral</td><td>GLOBAL</td></tr><tr><td>R.Thigh</td><td>V_R.Hip_JC</td><td>V_R.Knee_JC</td><td>R.Knee</td><td>Pelvis</td></tr><tr><td>L.Thigh</td><td>V_L.Hip_JC</td><td>V_L.Knee_JC</td><td>L.Knee</td><td>Pelvis</td></tr><tr><td>R.Shank</td><td>V_R.Knee_JC</td><td>V_R.Ankle_JC</td><td>R.Ankle</td><td>R.Thigh</td></tr><tr><td>L.Shank</td><td>V_L.Knee_JC</td><td>V_L.Ankle_JC</td><td>L.Ankle</td><td>L.Thigh</td></tr><tr><td>R.Foot</td><td>V_R.Ankle_JC</td><td>R.Toe</td><td>R.Ankle</td><td>R.Shank</td></tr><tr><td>L.Foot</td><td>V_L.Ankle_JC</td><td>L.Toe</td><td>L.Ankle</td><td>L.Shank</td></tr><tr><td>Trunk</td><td>V_Pelvis_Origin</td><td>V_Mid_Shoulder</td><td>R.Shoulder</td><td>Pelvis</td></tr><tr><td>Head/Neck</td><td>V_Mid_Shoulder</td><td>Top.Head</td><td>Front.Head</td><td>Trunk</td></tr><tr><td>R.UpperArm</td><td>R.Shoulder</td><td>R.Elbow</td><td>L.Shoulder</td><td>Trunk</td></tr><tr><td>L.UpperArm</td><td>L.Shoulder</td><td>L.Elbow</td><td>R.Shoulder</td><td>Trunk</td></tr><tr><td>R.Forearm</td><td>R.Elbow</td><td>R.Wrist</td><td>L.Elbow</td><td>R.UpperArm</td></tr><tr><td>L.Forearm</td><td>L.Elbow</td><td>L.Wrist</td><td>R.Elbow</td><td>L.UpperArm</td></tr><tr><td>R.Hand</td><td>R.Wrist</td><td>V_R.Hand</td><td>L.Wrist</td><td>R.Forearm</td></tr><tr><td>L.Hand</td><td>L.Wrist</td><td>V_L.Hand</td><td>R.Wrist</td><td>L.Forearm</td></tr><tr><td>PelvisWRTLab</td><td>V_Mid_Hip</td><td>V_Pelvis_Origin</td><td>V.Sacral</td><td>GLOBAL</td></tr><tr><td>TrunkWRTLab</td><td>V_Pelvis_Origin</td><td>V_Mid_Shoulder</td><td>R.Shoulder</td><td>GLOBAL</td></tr></tbody></table>



***

### **海伦海耶斯人体贴点示意图**

![](../.gitbook/assets/15.png) ![](../.gitbook/assets/16.png) ![](../.gitbook/assets/17.png) ![](../.gitbook/assets/18.png)

&#x20;                                                       Helenhayes FullBodyWithHead(29 Static)

<div align="center"><figure><img src="../.gitbook/assets/图片1 (1).png" alt="" width="195"><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/图片2 (1).png" alt="" width="195"><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/图片3 (1).png" alt="" width="195"><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/图片4 (1).png" alt="" width="195"><figcaption></figcaption></figure></div>

&#x20;                                                                  Helenhayes FullBody(26 Static)

<div><figure><img src="../.gitbook/assets/图片5 (1).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/图片6 (1).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/图片7 (1).png" alt=""><figcaption></figcaption></figure> <figure><img src="../.gitbook/assets/图片8 (1).png" alt=""><figcaption></figcaption></figure></div>

&#x20;                                                                  Helenhayes LowerBody(19 Static)
