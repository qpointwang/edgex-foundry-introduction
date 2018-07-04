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
