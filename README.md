![Hokkaido：后端开发、系统底层与数据](assets/hero.svg)

你好，我是 Hokkaido。写后端，也做系统底层和数据分析。这里放着我的系统实验、服务端项目和建模作品。

## 精选项目

<table>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/Hokkaidoooo/cs-systems-lab"><img src="https://raw.githubusercontent.com/Hokkaidoooo/cs-systems-lab/main/assets/cover.svg" alt="系统原理实验室：Cache、分页与 TCP Reno" width="100%"></a>
<h3>系统原理实验室</h3>
<p>在浏览器里观察 Cache 命中与替换、x86-64 页表寻址、TCP Reno 窗口变化。可以切换参数、回放轨迹，并用手算例子核对结果。</p>
<p><code>JavaScript</code> <code>Cache</code> <code>虚拟内存</code> <code>TCP</code></p>
<p><a href="https://hokkaidoooo.github.io/cs-systems-lab/">在线体验</a> · <a href="https://github.com/Hokkaidoooo/cs-systems-lab#第一次体验">操作示例与预期结果</a></p>
</td>
<td width="50%" valign="top">
<a href="https://github.com/Hokkaidoooo/supply-chain-risk-core"><img src="https://raw.githubusercontent.com/Hokkaidoooo/supply-chain-risk-core/main/assets/cover.svg" alt="产业链风险核心：路径传播、财务口径与数据契约" width="100%"></a>
<h3>产业链风险核心</h3>
<p>从工行杯参赛工程整理出的独立模块：沿有向图计算路径暴露，校验财务口径与版本化数据契约。附合成示例、预期数值和边界测试。</p>
<p><code>Python</code> <code>NetworkX</code> <code>图算法</code> <code>数据校验</code></p>
<p><a href="https://github.com/Hokkaidoooo/supply-chain-risk-core#快速运行">运行示例</a> · <a href="https://github.com/Hokkaidoooo/supply-chain-risk-core#模块阅读顺序">模块与接口</a></p>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/Hokkaidoooo/cpp-http-server"><img src="https://raw.githubusercontent.com/Hokkaidoooo/cpp-http-server/main/assets/cover.svg" alt="C++ HTTP 服务器：epoll、线程池与路由" width="100%"></a>
<h3>C++ HTTP 服务器</h3>
<p>Linux 下的 HTTP 服务原型，用 epoll 和线程池处理连接，按路由完成注册、登录校验与图片上传。代码包含请求解析、响应构造和 MongoDB 存取。</p>
<p><code>C++17</code> <code>epoll</code> <code>线程池</code> <code>MongoDB</code></p>
<p><a href="https://github.com/Hokkaidoooo/cpp-http-server#请求如何经过系统">请求处理流程</a> · <a href="https://github.com/Hokkaidoooo/cpp-http-server#运行">运行前提</a></p>
</td>
<td width="50%" valign="top">
<a href="https://github.com/Hokkaidoooo/mrp-system"><img src="https://raw.githubusercontent.com/Hokkaidoooo/mrp-system/main/assets/cover.svg" alt="MRP 物料需求计划系统：BOM 展开与逐层计算" width="100%"></a>
<h3>MRP 物料需求计划系统</h3>
<p>维护物料、BOM 与库存，输入顶层物料的分期计划下达量，沿 BOM 展开需求，按库存、提前期和批量规则生成计划订单。计算服务独立于页面和数据库访问。</p>
<p><code>Java</code> <code>Struts2</code> <code>Hibernate</code> <code>MySQL</code></p>
<p><a href="https://github.com/Hokkaidoooo/mrp-system">源码与模块说明</a> · <a href="https://github.com/Hokkaidoooo/mrp-system#构建与验证">构建与验证</a></p>
</td>
</tr>
</table>

## 其他项目

- [2023 数学建模国赛 B 题](https://github.com/Hokkaidoooo/cumcm-2023-multibeam)：多波束测线问题的团队参赛作品，包含[论文](https://github.com/Hokkaidoooo/cumcm-2023-multibeam/blob/main/paper/cumcm2023-b-paper.pdf)、四问代码与历史结果。
- [校园新闻门户](https://github.com/Hokkaidoooo/campus-news-portal)：Vue 2 门户页面与 Servlet/JSP 管理后台，展示新闻、通知和导航，使用 MySQL 存储。
- [南京气象可视化](https://github.com/Hokkaidoooo/nanjing-weather-visualization)：2023 年南京 365 天数据、5 类逐月图表和天气词云，可直接浏览 Notebook 与结果图。

## 开源参与

- [context-mode #1251](https://github.com/mksglu/context-mode/issues/1251)：Windows Hook 的依赖重复安装与控制台弹窗问题报告，涉及重试退避与 `windowsHide`。
