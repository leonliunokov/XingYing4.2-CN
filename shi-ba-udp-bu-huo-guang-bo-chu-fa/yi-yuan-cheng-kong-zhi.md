# （一）远程控制

1.  在数据广播面板的“捕获--远程”将开关启用（18.1.1），即开启了远程控制功能。其中端口是XINGYING接收控制命令的监听端口，默认为7060。如果系统中此端口被其它程序占用，请分配其它合适的端口给XINGYING使用。如果需要设置此端口，请先取消远程控制功能，修改完毕后再开启远程控制。\


    ![18.1.1](<../.gitbook/assets/0 (14).png>)
2. 开启远程控制后，需要连接镜头。当连接完成后，即可通过远程命令来控制录制。
3. 目前XINGYING支持的远程控制命令为XML文件格式：

* **开始触发**
* **停止触发**



***

### **开始通知**

1. 以下示例显示了开始通知。请注意，广播必须适合一个 UDP 数据包。
2. 以下示例中的缩进是为了清楚起见：实际的数据包没有缩进。标记之间的空白被删除。

\<?xml version="1.0" encoding="UTF-8" standalone="no" ?>

\<CaptureStart>

\<Name VALUE="Remotetake01"/>

\<SessionName VALUE="SessionName" />

\<Notes VALUE="Take notes if any"/>

< Delay VALUE="Reserved" />

\<Description VALUE="" />

\<DatabasePath VALUE="F:/shared/"/>

\<TimeCode VALUE="00:00:00:00"/>

\<PacketID VALUE="0"/>

\</CaptureStart>

### **说明：**

| Value            | Description |
| ---------------- | ----------- |
| Name             | 需要录制的文件名称   |
| SessionName      | 保留字段        |
| Notes            | 保留字段        |
| Description      | 保留字段        |
| Delay            | 保留字段        |
| DatabasePath（\*） | 录制文件路径      |
| TimeCode         | 保留字段        |
| PacketID         | 保留字段        |

### **注意：**

{% hint style="info" %}
如果当前工作环境加载了刚体/人体模版，那么参数DatabasePath需要与XINGYING当前工作目录一致，否则录制的文件无法直接在XINGYING的后处理中进行加载。

如果需要一个独立的录制文件路径，那么你也可以在录制结束后把使用的刚体/人体模版（.mars）文件拷贝到设定的录制文件夹中，这样就可以在XINGYING的后处理中进行正常加载。

对于需要录制未命名marker数据，只需要将参数DatabasePath设置为一个有效的路径即可。
{% endhint %}



***

### **停止通知**

1. 以下示例显示了停止通知。请注意，广播必须适合一个 UDP 数据包。
2. 以下示例中的缩进是为了清楚起见：实际的数据包没有缩进。标记之间的空白被删除。

\<?xml version="1.0" encoding="utf-8"?>

\<CaptureStop>

\<Name VALUE="Remotetake01" />

\<Notes VALUE="Take notes go here if any." />

\<Assets VALUE="skel1, skel2, sword" />

\<TimeCode VALUE="00:00:00:00" />

\<HostName VALUE="optional host name" />

\<ProcessID VALUE="optional process id" />

\</CaptureStop>

### 说明：

| Value    | Description |
| -------- | ----------- |
| Name     | 需要停止录制的文件名称 |
| Notes    | 保留字段        |
| Assets   | 保留字段        |
| TimeCode | 保留字段        |
| PacketID | 保留字段        |

### &#x20;<a href="#toc1844" id="toc1844"></a>
