# EdgeX-Foundry-Introduction
EdgeX Foundry 理解过程

### Definitions: "South Side" and "North Side"
**南侧**：物理领域内的所有物联网对象，以及与这些设备，传感器，执行器和其他物联网对象直接通信的网络边缘，并从中收集数据，统称为“南侧”。<br>
**北侧**：数据被收集，存储，聚合，分析和转换为信息的云（或企业系统），以及与云通信的网络部分，被称为网络的“北侧”。<br>
EdgeX可以根据需要和指示将数据“北”，“南”或横向发送。<br>

### EdgeX Foundry构建原则
EdgeX Foundry构思了以下的原则来指导整体的架构：<br>

**EdgeX Foundry与平台无关**
* 硬件
* 操作系统（Linux，Windows等）
* 分发 - 它必须允许通过边缘，网关，雾，云等微服务分发功能
* 协议和传感器无关<br>

**EdgeX Foundry必须非常灵活**
* 平台的任何部分都可以由其他微服务或软件组件进行升级，替换或扩充
* 允许服务根据设备功能和用例进行扩展和缩小
* EdgeX Foundry应该提供“参考实施”服务，但鼓励最好的解决方案<br>

**EdgeX Foundry必须提供存储和转发功能（以支持断开连接/远程边缘系统）**
**EdgeX Foundry必须支持并促进“智能”靠近边缘以便解决**
* 执行延迟问题
* 带宽和存储问题
* 远程操作问题<br>

**EdgeX Foundry必须支持棕色和绿色设备/传感器现场部署**
**EdgeX Foundry必须安全且易于管理**

### EdgeX Foundry服务层
EdgeX Foundry是一个开源微服务的集合。 这些微服务被组织成4个服务层，以及2个基础增强系统服务。服务层从物理领域的边缘从设备服务层遍历到导出服务层的信息领域的边缘，核心服务层位于中心。

EdgeX Foundry的4个服务层如下：

* Core Services Layer
* Supporting Services Layer
* Export Services Layer
* Device Services Layer

EdgeX Foundry的2个基础系统服务如下：

* Security
* System Management

![image](https://github.com/qpointwang/EdgeX-Foundry-Introduction/blob/master/Pic/EXF_Platform%20Architecture.png)

#### Core Services Layer
核心服务（CS）层将边缘处的北侧和南侧层分开。 核心服务包括以下组件：

* 核心数据：从南侧对象收集的数据的持久性存储库和相关的管理服务。
* 命令：处理北向应用发往南向设备的请求。
* 元数据：有关连接到EdgeX Foundry的对象的元数据的存储库和关联管理服务。 提供配置新设备并将其与其拥有的设备服务配对的功能。
* Registry and Config：为其他EdgeX Foundry微服务提供有关EdgeX Foundry和微服务配置属性（即初始化值存储库）中相关服务的信息。

此时EdgeX Foundry核心服务层包括以下微服务：

* Architecture--Core Services--Configuration and Registry
* Architecture--Core Services--Core Data
* Architecture--Core Services--Metadata
* Architecture--Core Services--Command
