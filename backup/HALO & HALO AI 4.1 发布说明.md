<h1>HALO 4.1 发布说明</h1>

<p><strong>软件更新 | 2025 年 2 月</strong><br>仅供研究使用</p>

<hr>

<h2>HALO v4.1</h2>

<h3>新功能</h3>
<ul>
  <li><strong>图像制作器（Figure Maker）：保存正在进行的图像以便稍后编辑</strong>
    <ul>
      <li>遵循 HALO Link 的研究级权限</li>
      <li>重新设计的布局，与新的 HALO Link 图像制作器保持一致</li>
    </ul>
  </li>
  <li><strong>图像视图设置应用</strong>
    <ul>
      <li>每个通道单独应用自动适配视图设置计算</li>
      <li>批量应用视图设置，无需导出/导入</li>
    </ul>
  </li>
  <li><strong>图像视图设置直方图</strong>
    <ul>
      <li>可比较多个已打开图像的直方图</li>
      <li>显示相对强度值</li>
      <li>显示真实伽马值和伽马曲线</li>
      <li>可使用对数视图</li>
    </ul>
  </li>
  <li><strong>高通量图像（highplexed images）表型设置优化</strong>
    <ul>
      <li>新的设置选择网格</li>
      <li>一次性为所有通道设定逻辑</li>
      <li>实时查看每个表型的调优标记</li>
      <li>分析标签页中显示表型预览列表</li>
      <li>支持将表型逻辑导出为 <code>.csv</code></li>
    </ul>
  </li>
  <li><strong>HALO 图像写入器生成 OME.TIFF 图像</strong>
    <ul>
      <li>拼接组件 <code>.qptiff</code></li>
      <li>融合的序列染色</li>
      <li>导出全分辨率图像</li>
      <li>静态标记图像</li>
    </ul>
  </li>
  <li><strong>更新的用户通知</strong>
    <ul>
      <li>所有通知显示在 HALO 右下角</li>
      <li>支持同时显示多个提醒</li>
      <li>点击即可关闭通知</li>
      <li>可选记录错误消息以便故障排查</li>
    </ul>
  </li>
</ul>

<hr>

<h2>分析模块更新</h2>
<ul>
  <li><strong>高维分析模块（High Dimensional Analysis） - 新增</strong>
    <ul>
      <li>无监督聚类</li>
      <li>降维图</li>
      <li>在图像、对象数据和图表之间保持交互性</li>
    </ul>
  </li>
  <li><strong>Highplex FL 模块 v5.0</strong>
    <ul>
      <li>支持阈值辅助（Threshold Assist）工作流</li>
      <li>支持上文所述的高通量表型设置优化</li>
    </ul>
  </li>
</ul>

<hr>

<h2>HALO AI</h2>
<ul>
  <li><strong>AI 标注工具改进</strong>
    <ul>
      <li>改进的 UI/UX</li>
      <li>支持多图像</li>
      <li>原生支持 FL 图像</li>
    </ul>
  </li>
  <li><strong>分类器流水线</strong>
    <ul>
      <li>标记下拉菜单显示分类器名称</li>
      <li>第一个标记叠加层显示最终步骤结果</li>
    </ul>
  </li>
  <li><strong>AI 应用（AI Apps）支持改进</strong>
    <ul>
      <li>简化批量分析</li>
      <li>在 HALO 界面中提供 AI Apps 用户指南</li>
    </ul>
  </li>
  <li><strong>额外的批量工作流</strong>
    <ul>
      <li>批量将分类器训练区域移动到标注标签页</li>
      <li>批量删除验证标注集</li>
    </ul>
  </li>
  <li><strong>支持导出最终定型的分类器</strong></li>
</ul>

<hr>

<h2>已移除的功能</h2>
<ul>
  <li><strong>手动点击计数器</strong> - 已由针状标注工作流替代</li>
  <li><strong>GRPC 服务器</strong> - 已由 GraphQL 服务器取代，成为唯一 API</li>
  <li>自 HALO v4.0 起，不再测试或正式支持与 eSlide Manager 的集成</li>
</ul>

<hr>

<h2>即将移除的功能</h2>
<p>无</p>

<hr>

<h2>Bug 修复</h2>

<h3>结果与导出</h3>
<ul>
  <li>当区域设置不同，无法生成自定义计算</li>
  <li>高级导出时检测到 OpenGL 错误</li>
  <li>批量处理后，分析结果和标记未立即显示</li>
  <li>加载相关结果/对象数据时延迟过长</li>
  <li>多研究高级导出报错</li>
  <li>高级导出在导出分析设置和标记缩略图时卡住</li>
  <li>TMA 高级导出未填充所有对象数据列</li>
</ul>

<h3>标注</h3>
<ul>
  <li>与 Concentriq 兼容的 5 点矩形标注</li>
  <li>旋转矩形标注会更改标注区域和分析区域</li>
  <li>截断的标注 regionID 导致选择异常</li>
  <li>在迁移过程中，旋转图像上的标注位置不正确</li>
  <li>导出 geoJSON 格式标注时报错</li>
  <li>导入的矩形标注无法复制</li>
  <li>反射和旋转图像上的画笔标注翻转</li>
  <li>“保存标注”按钮错误地处于启用状态</li>
  <li>导入标注失败 - 正文大小限制</li>
  <li>删除标注时的查看器导航行为不一致</li>
  <li>删除所有图层后无法保存标注</li>
  <li>多个平铺图像时标注工具栏被截断</li>
  <li>对多个小标注进行同心分区时出现多个错误提示</li>
</ul>

<h3>分析</h3>
<ul>
  <li>队列中重新提交旋转图像的 FOV 分析不保留旋转</li>
  <li>按优先级排序分析任务时报错</li>
  <li>即使分类器存在，仍显示“分析设置包含 HALO 中未找到的分类器”</li>
  <li>空间分析任务卡在队列中</li>
  <li>HALO 客户端在本地和批量分析中空间分析失败</li>
  <li>对标注区域的分析失败或跳过区域</li>
  <li>当实时调优窗口部分超出图像范围时，标记未显示</li>
  <li>分析设置中的重复名称导致 Multiplex IHC 中异常和错误汇总数据</li>
  <li>TMA 标签页中“分析整个图像和标注图层”选项仅对最后一层可见</li>
  <li>在渗透分析对象数据上完成空间分析失败</li>
  <li>当通道名称为数字时合并属性失败</li>
  <li>渗透分析可在无界面层情况下启动</li>
  <li>网络中断时标记图像绘制空白切片</li>
  <li>空间分析汇总数据导出缺少分析区域图层名称</li>
</ul>

<h3>分类器与 AI</h3>
<ul>
  <li>使用 AI 默认核分割时作业工作器卡死</li>
  <li>拥有者权限的标准用户无法保存分类器流水线</li>
  <li>AI 表型分类器在移动前不渲染分割</li>
  <li>选择分类器训练区域会跳转到未旋转位置</li>
  <li>在旋转图像中对未旋转区域进行分类器训练</li>
  <li>难以从标记中选择孤立的分类器对象</li>
  <li>Slide QCv3 和 AI Apps 未标记为预训练分类器，可被覆盖</li>
  <li>GPU 作业被 CPU 节点接管用于重新提交的分析</li>
  <li>加载分类器窗口有时加载缓慢</li>
  <li>非连续类别 ID 的对象表型验证对象数据错误</li>
  <li>未保存的 AI 分类器在默认 2500 次迭代检查点抛出未处理异常</li>
  <li>HALO-only 客户端无法批量提交嵌入式 AI 模块分析</li>
  <li>分类器名称超过 100 个字符时提交作业触发 GraphQL 错误</li>
  <li>删除已保存的预训练分割分类器时同时删除权重文件</li>
  <li>带有额外训练的 SlideQCv2 模型无法导入</li>
  <li>注册的跨图像模态序列切片上的嵌入分类器失败</li>
  <li>在分类器标签页修改画笔标注无效</li>
  <li>允许为分析和分类器标记设置不同透明度</li>
</ul>

<h3>图像查看器</h3>
<ul>
  <li>改进图像切片加载与渲染</li>
  <li>移动查看器时标记图像闪烁</li>
  <li>HALO 将 ER.QPTIFF 图像读取为 12 位，截断 14/16 位</li>
  <li>改进 10/12/14 位图像的读写支持</li>
  <li>在图像标签页间切换时卡顿</li>
  <li>关闭图像时报未处理异常</li>
  <li>FL 通道显示的像素强度值不正确</li>
  <li>区域设置导致视图设置导入错误</li>
  <li>浮动通道框时关闭图像导致其消失</li>
  <li>HALO 快照不包含比例尺</li>
  <li>RTT 的标记按钮在关闭后切换图像时无响应</li>
  <li>NDPI 错误 - 文件过大：更新 SDK</li>
  <li>初始白值与分辨率导致 Hyperion 图像显示异常</li>
  <li>无法打开未知压缩格式的 VSI 图像</li>
  <li>显示 FL 像素强度时，平铺 FL 图像触发异常</li>
  <li>支持 Morphle Labs 的稀疏平铺 DICOM 图像</li>
  <li>打开带不可访问标记图像时报异常</li>
  <li>MIBI .TIFF 融合图像的通道最大值被截断</li>
  <li>FL ImageJ TIFF 的通道最大值不正确</li>
  <li>支持多文件 OME.TIFF</li>
  <li>图像缩放与实时调优窗口存在差异</li>
  <li>打开相差 CZI 图像时报错</li>
  <li>序列染色融合的通道最大值未正确转换</li>
  <li>对分块/条带式 SVS 性能优化</li>
  <li>对 .LIF Z 轴堆栈图像添加无效文件错误提示</li>
  <li>改进一次打开 18+ 图像的加载</li>
  <li>打开 .LIF 裁剪源图像时报错</li>
  <li>更容易关闭 FL 通道颜色选择器</li>
  <li>QuPath 裁剪的 16 或 32 位 OME-TIFF 无法正确打开</li>
  <li>图像制作器中无法添加含多个已打开图像的面板</li>
</ul>

<h3>配准</h3>
<ul>
  <li>FL 序列染色图像的对齐问题</li>
  <li>在非活动图像上放置配准标记时不显示</li>
  <li>配准过程中分辨率值不正确或为 0 时触发异常</li>
  <li>批量图像配准 <code>.MRXS</code> 文件时报错</li>
</ul>

<h3>系统</h3>
<ul>
  <li>选择不同研究后图像列表延迟加载</li>
  <li>无法将裁剪图像保存到 NAS</li>
  <li>HALO Link 用户组权限阻止分割 TMA 分割显示</li>
  <li>API 网关未正确处理 "CloseReceived" 状态</li>
  <li>HALO 安装程序间歇性丢失 segment anything 模型权重文件</li>
  <li>提高迁移性能，使标记图像宽度与分析任务区域宽度匹配</li>
  <li>增加 SQL 和 SignalR 超时默认值</li>
  <li>无法创建离线安装包</li>
  <li>在 ASP.NET Cookies 中添加 "secure"</li>
  <li>GraphQL Workbench 的工具提示卡住显示</li>
  <li>非正常退出后 HALO 无法启动</li>
</ul>

<hr>

<blockquote>
<p>每个 HALO 版本都会新增功能和更新模块。<br>这些改进可能会导致不同版本 HALO 的分析结果略有差异。</p>
</blockquote>

<p>如需更多信息或有任何问题，请联系 <strong>support@indicalab.com</strong></p>

<p>访问 <strong><a href="https://learn.indicalab.com/">Indica Labs 在线学习门户</a></strong> 以了解更多新功能信息。</p><!--##{"timestamp":1738398581}##-->