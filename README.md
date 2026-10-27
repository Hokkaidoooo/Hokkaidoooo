![Hokkaido：后端架构、系统底层与可验证 Agent](assets/hero.svg)

### 关于 / About

专注于**系统底层、服务端架构与可验证 AI 智能体（Verifiable Agents）**。  
倾向于通过明确的抽象边界、确定性状态机与可复现的评测结果构建可靠系统。日常核心技术栈为 C++17、Python 与 Linux。

[个人作品集](https://hokkaidoooo.github.io/) · [技术手记](https://hokkaidoooo.github.io/blog/) · [GitHub 仓库列表](https://github.com/Hokkaidoooo?tab=repositories) · 📍 南京

---

## 核心项目 / Projects

### 01 / [TraceDesk](https://github.com/Hokkaidoooo/tracedesk) · 智能客服与可验证 Agent
> 带版本化证据溯源、LangGraph 双角色核验与受约束售后事务的 AI 客服系统。  
> `Python 3.12` `LangGraph` `GraphRAG` `FastAPI` `Neo4j` `TypeScript` · [v0.2.0 Release](https://github.com/Hokkaidoooo/tracedesk/releases/tag/v0.2.0)

- **版本化证据绑定**：上传资料绑定发布快照、原文页码与 SHA-256 散列；集成 MinerU 与 RRF 混合检索，历史查询固定快照版本，杜绝上下文漂移。
- **双角色核验机制**：基于 LangGraph 实现「研究角色规划取证」+「公共验证角色交叉核验」双轨工作流，并与单研究者基线进行消融对比。
- **确定性售后事务**：严格隔离模型生成与业务状态，退款资格、金额核算与订单状态由服务端规则状态机原子执行，要求卡片显式二次确认。
- **文档与验证**：[架构设计与模型边界](https://github.com/Hokkaidoooo/tracedesk/blob/main/docs/architecture.md) · [评测消融验证](https://github.com/Hokkaidoooo/tracedesk/blob/main/docs/validation-v0.2.md) · [源码仓库 ↗](https://github.com/Hokkaidoooo/tracedesk)

---

### 02 / [cpp-http-server](https://github.com/Hokkaidoooo/cpp-http-server) · Linux C++17 服务端
> 增量状态机解析、非阻塞 epoll 统一调度与真实压测分析。  
> `C++17` `Linux` `epoll` `ThreadPool` `MongoDB` `CMake/Ninja`

- **I/O 与并发模型**：单个 epoll 线程增量解析 HTTP 请求，就绪请求附带单调自增代号推入有界队列（容量 64）；过载时快速失败返回 503，避免请求堆积雪崩。
- **内存安全与连接回收**：工作线程仅处理请求值、不持有套接字，通过 eventfd 完成队列通知主线程关闭或回发；CI 通过 ASan、UBSan 与 TSan 全项检查。
- **真实压测与瓶颈剖析**：CI Ubuntu 22.04 runner 实跑 `hey` 压测（并发 64 达 12,409 req/s @ P50 4.9ms），分析记录了工作线程数增加导致上下文切换开销反超并行收益的测量结论。
- **文档与验证**：[请求处理流程](https://github.com/Hokkaidoooo/cpp-http-server#结构) · [CI 压测原始数据与分析](https://github.com/Hokkaidoooo/cpp-http-server#性能) · [构建与验证](https://github.com/Hokkaidoooo/cpp-http-server#linux-构建与验证入口) · [源码仓库 ↗](https://github.com/Hokkaidoooo/cpp-http-server)

---

### 03 / [cs-systems-lab](https://github.com/Hokkaidoooo/cs-systems-lab) · 系统原理交互式实验室
> 在浏览器中交互式观察 Cache 替换、x86-64 四级页表与 TCP Reno 拥塞控制。  
> `JavaScript` `Cache` `Virtual Memory` `TCP Reno` · [👉 立即在线体验](https://hokkaidoooo.github.io/cs-systems-lab/)

- **Cache 替换模拟**：支持直接映射、全相联与组相联；输入访问序列即可同屏对比回放 LRU 与 FIFO 的命中/失效与替换轨迹。
- **四级页表地址翻译**：可视化分解 PML4、PDPT、PD、PT 索引与物理偏移，直观展示稀疏访问下的页表内存物理占用。
- **TCP Reno 拥塞控制**：逐步单步模拟慢启动、拥塞避免、快速重传与快速恢复，曲线实时联动内部状态变量（cwnd / ssthresh）。
- **文档与验证**：[操作示例与手算例核对](https://github.com/Hokkaidoooo/cs-systems-lab#第一次体验) · [源码仓库 ↗](https://github.com/Hokkaidoooo/cs-systems-lab)

---

### 04 / [zhihu-column-exporter](https://github.com/Hokkaidoooo/zhihu-column-exporter) · 知乎专栏离线归档
> 将专栏完整导出为 Markdown、离线 HTML 与本地图片的 Chrome 扩展。  
> `TypeScript` `Chrome Extension` `Manifest V3` `Node.js` · [v1.5.1 安装包](https://github.com/Hokkaidoooo/zhihu-column-exporter/releases/latest)

- **自适应抓取与归档**：自动分页读取标准专栏全量目录；接口与前台标签页双模式降级；导出带独立阅读目录、相对路径图片与离线 HTML。
- **断点补读与权限安全**：失败章节生成清单，支持一键单独补读未完成内容；严格采用零 Cookie 权限设计，沿用浏览器自身正常登录态。
- **文档与验证**：[使用说明](https://github.com/Hokkaidoooo/zhihu-column-exporter#使用) · [开发与测试规范](https://github.com/Hokkaidoooo/zhihu-column-exporter/blob/main/DEVELOPMENT.md) · [源码仓库 ↗](https://github.com/Hokkaidoooo/zhihu-column-exporter)

---

### 05 / [supply-chain-risk-core](https://github.com/Hokkaidoooo/supply-chain-risk-core) · 产业链风险与授信核心
> 工行杯参赛工程整理的 Python 分析包：工商财务特征、网络传导与报告复现。  
> `Python` `NetworkX` `NumPy` `图算法` · [决赛分析成品与合成案例](https://github.com/Hokkaidoooo/supply-chain-risk-core#运行完整案例)

- **图传导情景模拟**：基于 NetworkX 构建上下游依赖拓扑，计算最强路径系数连乘传导，量化关键节点断裂对终端企业的风险敞口。
- **数据契约与规则引擎**：建立明确的数据输入校验与财务评分规则，全流程自动化复现决赛分析报告。
- **文档与验证**：[模块与接口规范](https://github.com/Hokkaidoooo/supply-chain-risk-core#已收录的能力) · [源码仓库 ↗](https://github.com/Hokkaidoooo/supply-chain-risk-core)

---

### 06 / [cumcm-2023-multibeam](https://github.com/Hokkaidoooo/cumcm-2023-multibeam) · 数模国赛 B 题 · 多波束测线优化
> 2023 数学建模国赛 B 题团队作品：论文复现、几何推导与覆盖约束复核。  
> `Python` `MATLAB` `数模国赛` `几何建模` · [参赛论文 PDF](https://github.com/Hokkaidoooo/cumcm-2023-multibeam/blob/main/paper/cumcm2023-b-paper.pdf)

- **坡度修正几何模型**：推导换能器开角 $2\theta=120^\circ$ 在任意坡度 $\alpha$ 下的多波束覆盖宽度与重叠率公式。
- **约束验算与测线设计**：结合网格化海底地形，以测线总里程最短为目标建立优化模型，逐格复核 10%~20% 覆盖重叠约束。
- **文档与验证**：[几何推导与复核代码](https://github.com/Hokkaidoooo/cumcm-2023-multibeam#结构) · [源码仓库 ↗](https://github.com/Hokkaidoooo/cumcm-2023-multibeam)

---

## 其他工程 / Other Works

- [MRP 物料需求计划系统](https://github.com/Hokkaidoooo/mrp-system)：按 BOM 拓扑逐层展开需求，在单一数据库事务中替换整批计算结果，含失败回滚与并发重算验证。
- [校园新闻门户](https://github.com/Hokkaidoooo/campus-news-portal)：Vue 2 前台 + Servlet/JSP 管理后台，统一连接池管理与登录会话控制。
- [南京气象数据可视化](https://github.com/Hokkaidoooo/nanjing-weather-visualization)：离线校验南京 2023 年 365 天天气数据，Notebook 与脚本共用流程生成 61 张图表。

---

## 开源参与 / Open Source

- [mksglu/context-mode #1251](https://github.com/mksglu/context-mode/issues/1251)：排查并提交 Windows Hook 依赖重复安装与控制台弹窗问题报告，分析重试退避机制与 `windowsHide` 参数行为。
