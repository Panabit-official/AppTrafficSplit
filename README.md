# 🌐 **背景**
在传统网络架构中，流量分流通常依赖静态规则（Static Rules），例如基于 **IP 地址**、**端口号**、**协议类型** 等预定义策略进行流量调度。虽然这种方式在固定环境下能够有效工作，但随着业务需求的不断变化和网络环境的日益复杂，**静态规则的灵活性和适应性不足**，导致诸多问题。

---

## 🔥 **传统流量分流面临的挑战**

### 🔹 **缺乏灵活性，难以适应动态业务需求**  
- 依赖固定规则（IP、端口、协议），无法应对 **IP 变更、业务扩展、突发流量** 等情况。  
- 规则更新需手动维护，**运维成本高**，难以做到实时调整。  

### 🔹 **难以精准识别流量，缺乏智能调度能力**  
- 无法识别 **加密流量、动态端口或应用层协议**，导致分流策略失效。  
- 无法基于实时网络状态（**带宽、时延、负载**）进行动态调整，影响**流量优化**和**QoS 保障**。

---

## 🚀 **新型流量分流：灵活、智能、高效**

新型流量分流方式基于 **应用类型**进行智能调度，将 **不重要的娱乐应用** 无感知地分流到普通线路上，同时提供更大的可操作空间，以解决传统方式的局限性。

### 🎯 **多样化的分流方式**
支持多种匹配方式：  
- **五元组**（源 IP、目标 IP、源端口、目标端口、协议）  
- **应用协议**（如 HTTP、HTTPS、DNS）  
- **域名匹配**（如 `*.tiktok.com`、`*.netflix.com`）  
- **VLAN**、**网络接口**、**用户类型**等  

### 🎯 **精准的应用识别**
- 识别率高达 **95%+**，能够识别并控制 **14 大类、上千种应用**，确保流量精准分流。

### 🎯 **多样的链路接入方式**
支持超过 **2000+ 条线路接入**，包括：
- **DHCP**
- **静态 IP**
- **PPPOE 拨号**
- **L2TP**

### 🎯 **高性能的转发能力**
支持最高：
- **100G 吞吐**
- **1800 万并发连接**
- **全场景接入**，保障流量分流高效顺畅。

---

## 🌟 **总结**
- 传统的静态规则已经无法满足日益复杂的网络需求，智能化、灵活的流量分流解决方案成为必然选择。
- 新型流量分流不仅可以应对动态变化的网络环境，还能提供精准流量识别和智能调度，保证网络的高效和稳定运行。

---

## 三．典型案例  

### **📌 3.1 xx 网络业务分流案例**  

#### **项目背景**  
某企业主要业务为**政企专线接入**，随着业务增长，**专线资源紧张**，高峰时段**网络不稳定**。  
面对这一问题，原方案为**扩容专线**，但整体**成本过高**，需寻找更优方案。  

#### **解决方案**  
采用 **Panabit 网关** 透明接入至 **内网核心交换机 & 出口交换机** 之间，**监测 2 天流量**后，将用户**感知体验较小的娱乐应用**调度至 **移动链路**，以降低原有**专线负载**，提升用户体验。

#### **分流成果**  
📈 **分流效果显著**：
- **40%** 总流量被成功分流  
- **用户体验无明显变化**  

📌 **带宽利用率提升**：
- 原电信专线总带宽 **500M**
- 设备接入后高峰期 **600M+**
- **提升专线使用率 & 改善用户体验**  

📌 **流量趋势变化**：
- **下行流量高峰期分流 200M**
- **上行流量高峰期分流 100M**
- **节省 40% 以上的带宽压力**  

📊 **总流量上下行趋势**：
![总流量趋势](assets/total_traffic.png)  

📊 **分流链路下行流量趋势**：
![下行趋势](assets/downstream.png)  

📊 **分流链路上行流量趋势**：
![上行趋势](assets/upstream.png)  

---

## 四．基本配置  

### **🔹 1. NAT 分流策略**  
📌 **路径**： `【网络设置】->【路由/NAT】`  
📌 **步骤**：
1. 添加策略，填写序号  
2. 选择分流协议（如**网络游戏**）  
3. 选择 NAT 线路  
4. 点击 **确认**，完成部署  

📌 **示例截图**：  
![NAT 配置](assets/nat_config.png)  

---

### **🔹 2. 自定义协议（以网易协议为例）**  
📌 **路径**：
- `【应用识别】 -> 【自定义协议名称】 -> 【域名关联】`  
- 添加 **域名 & 端口**，选择所属协议  

📌 **步骤一**：
![自定义协议](assets/custom_protocol_step1.png)  
![域名关联](assets/custom_protocol_step2.png)  

📌 **步骤二**：
- 进入 `【网络设置】 -> 【路由/NAT】`  
- 选择 **自定义协议**，并选择 NAT **特权线路**  
- **点击确认**，完成部署  

📌 **示例截图**：  
![NAT 配置](assets/custom_protocol_step3.png)  

# 📞 联系我们  

获取更多信息，请访问 [Panabit 官网](https://www.panabit.com/)。
