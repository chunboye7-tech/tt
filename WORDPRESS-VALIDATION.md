# XIUJIN WordPress 1.1.0 验证报告

最终发布构建已完成，所有阻断项为零。

| 检查范围 | 结果 |
|---|---:|
| WordPress 主题静态检查 | 80 通过 / 0 失败 / 1 预期提示 |
| 浏览器端到端检查 | 84 / 84 通过 |
| XIUJIN Store Core 插件 | 35 / 35 通过 |
| 国际化与语言包 | 22 / 22 通过 |
| PHP AST 语法解析 | 30 / 30 文件通过 |
| 发布包完整性 | 40 / 40 通过 |

主题检查中的唯一提示是：主题自身没有询价提交处理器。该职责有意交给同一交付中的 `XIUJIN-Store-Core-1.1.0.zip`，因此不是缺陷。

## 图片与 3D 模型专项核验

六张产品图片已分别绑定六个对应的 3D 外观，内部模型索引为 `0, 1, 4, 5, 2, 3`：

1. Black / ivory → Black / ivory
2. Red / black with color trim → Red / black with color trim
3. Black / white with blue piping → Blue / white
4. Black / yellow → Yellow / black
5. Red / black shaped cushions → Red / black
6. Black / orange fabric → Orange / black

浏览器验证覆盖：六组映射声明、加载 3D 前的选择同步、按需加载后保持所选模型、依次切换全部六款、桌面与移动端布局、图片解码、控制台错误、网络失败、减少动态效果和水平溢出。

## 浏览器验证明细

- 视口：1440、768、390、320 px
- 商品卡：18
- 首页真实配置：6
- 展厅图：10
- 3D：点击后按需加载
- `8011`：公开首页不显示
- Shopify 运行依赖与网络请求：0
- 控制台错误、未捕获错误、失败请求：0
- 减少动态效果：通过
- 累积布局偏移：0.0000
- 主线程长任务时间：0 ms

## 数据与多语言验证

- 商品系列：18
- 视觉配置：58
- 商品媒体：118
- 商品导入状态：全部为草稿
- 价格字段：全部留空
- 商品翻译稿：西班牙语 18 行、葡萄牙语（巴西）18 行
- 主题固定文案：ES 240 / 240，PT-BR 240 / 240
- 插件固定文案：ES 77 / 77，PT-BR 77 / 77
- 主题运行时文件：`languages/es_ES.mo`、`languages/pt_BR.mo`（按 WordPress 主题文本域规则校验）

## 发布包验证

主题、插件、商品导入、预览、源码和完整合集的 CRC、安全路径、重复成员、目录结构、源文件一致性、组件字节一致性和可复现构建均已核验。最终结果为 40 / 40 通过。

对应机器可读证据收录于 `XIUJIN-WordPress-Complete-1.1.0.zip` 和 `XIUJIN-WordPress-Source-1.1.0.zip`。
