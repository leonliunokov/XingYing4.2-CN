# （二）远程触发

1.  在数据广播面板的“捕获--触发”将开关启用（18.2.1），即开启了远程触发功能。其中端口是XINGYING发送控制命令的广播端口，默认为7061。如果第三方软件或者工具监听的端口为其它端口，请分配正确的端口给XINGYING使用。如果需要设置此端口，请先取消远程触发功能，修改完毕后再开启远程触发。\


    ![18.2.1](<../.gitbook/assets/1 (11).png>)
2. 开启远程触发后，需要连接镜头。当连接完成后，即可通过开启/停止录制来进行触发。
3. 目前XINGYING发送的触发控制命令为XML文件格式：
   * **开始触发**
   * **停止触发**



***

### **开始触发**

1. 以下示例显示了开始触发。请注意，广播必须适合一个 UDP 数据包。
2. 以下示例中的缩进是为了清楚起见：实际的数据包没有缩进。标记之间的空白被删除。

\<?xml version="1.0" encoding="UTF-8" standalone="no" ?>

\<CaptureStart>

\<Name VALUE="RemoteTriggerTest\_take0116" />

\<DatabasePath VALUE="F:\20230712\test1" />

\<Notes VALUE="This is Beijing NOKOV Science & Technology Co., Ltd Motion Capture Start Msg" />

\<Description VALUE="NULL" />

\<Delay VALUE="33" />

\<PacketID VALUE="10028" />

\</CaptureStart>

### 说明：

| Value        | Description |
| ------------ | ----------- |
| Name         | 录制的文件名称     |
| SessionName  | 保留字段        |
| Notes        | 保留字段        |
| Description  | 保留字段        |
| Delay        | 保留字段        |
| DatabasePath | 录制的文件路径     |
| PacketID     | 保留字段        |

#### &#x20;<a href="#toc8689" id="toc8689"></a>

***

### **停止触发**

1. 以下示例显示了停止触发。请注意，广播必须适合一个 UDP 数据包。
2. 以下示例中的缩进是为了清楚起见：实际的数据包没有缩进。标记之间的空白被删除。

\<?xml version="1.0" encoding="UTF-8" standalone="no" ?>

\<CaptureStop RESULT="SUCCESS">

\<Name VALUE="RemoteTriggerTest\_take0114" />

\<DatabasePath VALUE="F:\20230712\test1" />

\<Notes VALUE="This is Beijing NOKOV Science & Technology Co., Ltd Motion Capture Stop Msg" />

\<Description VALUE="NULL" />

\<Delay VALUE="33" />

\<PacketID VALUE="10025" />

\</CaptureStop>

### 说明：

<table data-header-hidden><thead><tr><th width="377"></th><th></th></tr></thead><tbody><tr><td>Value</td><td>Description</td></tr><tr><td>Name</td><td>录制的文件名称</td></tr><tr><td>SessionName</td><td>保留字段</td></tr><tr><td>Notes</td><td>保留字段</td></tr><tr><td>Description</td><td>保留字段</td></tr><tr><td>Delay</td><td>保留字段</td></tr><tr><td>DatabasePath</td><td>录制的文件路径</td></tr><tr><td>PacketID</td><td>保留字段</td></tr></tbody></table>
