![Hokkaido：后端开发、系统底层与数据](assets/hero.svg)

你好，我是 Hokkaido。写后端，也做系统底层和数据分析。这里放着我的系统实验、服务端项目和建模作品。

## 精选项目

<table>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/Hokkaidoooo/cs-systems-lab"><img src="https://raw.githubusercontent.com/Hokkaidoooo/cs-systems-lab/main/assets/cover.svg" alt="系统原理实验室：Cache、分页与 TCP Reno" width="100%"></a>
<h3>系统原理实验室</h3>
<p>在浏览器里观察 Cache、页表和 TCP Reno。支持 LRU/FIFO 同步回放和完整实验链接，结果用手算例、固定种子性质测试与真实浏览器操作核对。</p>
<p><code>JavaScript</code> <code>Cache</code> <code>虚拟内存</code> <code>TCP</code></p>
<p><a href="https://hokkaidoooo.github.io/cs-systems-lab/">在线体验</a> · <a href="https://github.com/Hokkaidoooo/cs-systems-lab#第一次体验">操作示例与预期结果</a></p>
</td>
<td width="50%" valign="top">
<a href="https://github.com/Hokkaidoooo/supply-chain-risk-core"><img src="https://raw.githubusercontent.com/Hokkaidoooo/supply-chain-risk-core/main/assets/cover.svg" alt="产业链风险核心：路径传播、财务口径与数据契约" width="100%"></a>
<h3>产业链风险分析与授信研究</h3>
<p>从工行杯参赛工程整理出的 Python 包，串联工商财务特征、评分授信、产业链传导与报告复现。附可运行的合成案例和本人编制的决赛分析成品。</p>
<p><code>Python</code> <code>NetworkX</code> <code>图算法</code> <code>数据校验</code></p>
<p><a href="https://github.com/Hokkaidoooo/supply-chain-risk-core#运行完整案例">运行示例</a> · <a href="https://github.com/Hokkaidoooo/supply-chain-risk-core#已收录的能力">模块与接口</a></p>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/Hokkaidoooo/cpp-http-server"><img src="https://raw.githubusercontent.com/Hokkaidoooo/cpp-http-server/main/assets/cover.svg" alt="C++ HTTP 服务器：epoll、线程池与路由" width="100%"></a>
<h3>C++ HTTP 服务器</h3>
<p>实现分段 HTTP 请求解析、Argon2id 登录会话和 PNG 上传，连接由 epoll 线程统一管理。真实 MongoDB 集成测试覆盖并发回收，并通过 ASan/UBSan 与 TSan 检查。</p>
<p><code>C++17</code> <code>epoll</code> <code>线程池</code> <code>MongoDB</code></p>
<p><a href="https://github.com/Hokkaidoooo/cpp-http-server#结构">请求处理流程</a> · <a href="https://github.com/Hokkaidoooo/cpp-http-server#linux-构建与验证入口">构建与验证</a></p>
</td>
<td width="50%" valign="top">
<a href="https://github.com/Hokkaidoooo/mrp-system"><img src="https://raw.githubusercontent.com/Hokkaidoooo/mrp-system/main/assets/cover.svg" alt="MRP 物料需求计划系统：BOM 展开与逐层计算" width="100%"></a>
<h3>MRP 物料需求计划系统</h3>
<p>按 BOM 拓扑展开需求，FOQ 按整批补足，并保留期外下达量。重算在一个事务中替换整批结果，包含真实数据库失败回滚、并发重算和 Tomcat 部署验证。</p>
<p><code>Java</code> <code>Struts2</code> <code>Hibernate</code> <code>MySQL</code></p>
<p><a href="https://github.com/Hokkaidoooo/mrp-system">源码与模块说明</a> · <a href="https://github.com/Hokkaidoooo/mrp-system#构建与验证">构建与验证</a></p>
</td>
</tr>
</table>

## 其他项目

- [2023 数学建模国赛 B 题](https://github.com/Hokkaidoooo/cumcm-2023-multibeam)：保留团队参赛[论文](https://github.com/Hokkaidoooo/cumcm-2023-multibeam/blob/main/paper/cumcm2023-b-paper.pdf)与历史结果，新增共享几何推导、逐格差异和覆盖约束验算。
- [校园新闻门户](https://github.com/Hokkaidoooo/campus-news-portal)：Vue 2 门户与 Servlet/JSP 后台，统一连接池、登录控制和 PNG 存储，支持不同部署上下文和端口。
- [南京气象可视化](https://github.com/Hokkaidoooo/nanjing-weather-visualization)：离线校验 2023 年 365 天数据，脚本与 Notebook 共用流程生成 61 张图，保留原始数据与历史图片。

## 开源参与

- [context-mode #1251](https://github.com/mksglu/context-mode/issues/1251)：Windows Hook 的依赖重复安装与控制台弹窗问题报告，涉及重试退避与 `windowsHide`。
