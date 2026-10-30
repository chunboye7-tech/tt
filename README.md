# XIUJIN WordPress + WooCommerce 网站

这是为 **Bazhou Xiujin Furniture Co., Ltd / XIUJIN** 制作的 WordPress 网站，面向办公椅、电竞椅和行政办公椅的工厂批发与零售询价。

![XIUJIN WordPress 首页预览](XIUJIN-WordPress-preview-desktop.png)

## 现在安装哪个文件

如果当前网站已经安装 XIUJIN 主题和 Store Core，本次只需进入 **外观 → 主题 → 安装主题 → 上传主题**，上传并替换：

- [`XIUJIN-WordPress-Theme-1.3.4.zip`](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-Theme-1.3.4.zip)

本次重新设计页眉右侧比例：Facebook 与 TikTok 合并成紧凑的浅色图标组，紧邻等高的 WhatsApp 按钮，消除原来的大空隙并改善桌面和手机观感。已经安装并正常工作的 Store Core 1.2.1 至 1.3.3 可以保留；本次插件运行逻辑未改，无需重新配置询价、SMTP 或广告追踪。

首次建站请同时安装 1.3.4 主题和 Store Core 插件。`XIUJIN-WordPress-Complete-1.3.4.zip` 是供电脑解压的完整交付合集，不能直接在 WordPress 的“上传插件”或“上传主题”页面安装。

## 下载文件

- [询价与广告追踪插件 1.3.4](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-Store-Core-1.3.4.zip)
- [WordPress 主题 1.3.4](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-Theme-1.3.4.zip)
- [WooCommerce 商品导入包：18 个系列、58 个配置、118 张媒体](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WooCommerce-Import-18-Series-58-Configurations.zip)
- [完整交付包：主题、插件、商品包、报告和预览](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-Complete-1.3.4.zip)
- [可复现构建源码](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-Source-1.3.4.zip)
- [本地交互预览](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-Preview.zip)
- [手机端预览图](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-preview-mobile.png)

详细步骤见 [Hostinger 安装说明](HOSTINGER-INSTALL-中文.md)，文件用途见 [先从这里开始](START-HERE-中文.md)。

## 1.3.4 页眉比例与观感优化

- Facebook 与 TikTok 归入同一个浅色圆角图标组，并紧邻 WhatsApp，页眉不再出现不自然的大空隙。
- 社交图标缩为 30 × 30 px，WhatsApp 与图标组保持相近高度；阴影、边框和品牌色已统一收敛。
- 320、360、390、768、1024 和 1440 px 均已通过无横向溢出检查，桌面与手机端均无裁切或按钮碰撞。

## 1.3.3 页眉社交入口

- 页眉默认显示 Facebook 与 TikTok 图标，分别跳转到已确认的主页；所有图标使用本地内联 SVG，不依赖第三方图标脚本。
- Telegram 保留为后续可选入口，链接为空时自动隐藏；Instagram 不在页眉显示。
- WhatsApp 默认号码更新为 `+852 9019 9249`，跳转地址为 `https://wa.me/85290199249`。
- 320、360、390、768、1024 和 1440 px 均已通过无横向溢出检查；图标包含键盘焦点和辅助技术标签。

## 1.3.2 工厂实拍媒体优先展示

- 工厂实拍图册与仓库视频现位于主视觉和数据条之后，成为访客进入首页后看到的第一内容版块；产品分类、目录、3D 和询价内容继续排列在后方。
- 删除原来的三张 AI 工厂示意图，落地页改为用户提供的四张生产现场照片、真实成品仓库视频与经哈希核验的封面。
- 工厂照片展示 CNC 木件加工、面料卷上料、多层面料裁剪、泡棉与软包准备；标题和说明仅描述画面中可核实的内容。
- 桌面端使用重点图与工序图分层排版，手机端改为清晰单列；照片延迟加载，点击后通过原生 `dialog` 放大查看，并支持键盘关闭与焦点返回。
- 视频已移除音轨并压缩为网页版本，默认不自动播放；访客点击播放，移动端与桌面端均有响应式布局。
- 页面文案只描述视频中可验证的成品仓储、纸箱库存和发货准备场景，不把同一段视频误称为组装或质检工序。
- 英语、西班牙语和葡萄牙语固定文案已同步完成。

## 1.2.2 语言切换修复

- 产品页、隐私政策等已有关联译本的页面，切换语言时进入对应翻译页，不再强制返回该语言首页。
- 语言下拉框已补充辅助技术可识别的名称。
- 这一行为取决于 Polylang 后台已将英语、西班牙语和葡萄牙语内容正确关联。

## 1.2.1 询价修复

- 修复首页商品卡进入询价区后未自动带入商品名称的问题。
- 自动带入当前页面语言的商品名称，适用于英语、西班牙语和葡萄牙语。
- 新增正式 Store Core 表单回归检查；插件检查现为 48 / 48 通过。

## 1.2.0 新增广告衡量

- 在 **设置 → XIUJIN tracking** 中配置 Google Ads 转化 ID/标签、Meta Pixel ID、TikTok Pixel ID，以及可选的 GA4 Measurement ID。
- 所有 ID 默认为空；空值时不会加载追踪脚本，也不会生成询盘转化标记。
- Google、Meta、TikTok 标签只在访客明确接受分析和广告后加载；访客可以改回“仅必要功能”。
- WordPress 邮件程序接受一条有效询盘发送后，各平台只接收一次匿名 Lead/SubmitForm 事件和随机事件编号。
- 姓名、邮箱、电话、公司、产品要求和留言不会回传给广告平台。
- 如果 Site Kit、MonsterInsights 或 GTM 已加载 GA4，请把本插件的 GA4 字段留空，避免重复页面浏览。严格要求同意前零第三方请求时，还需关闭其他插件的前端分析输出或统一使用同一个 CMP。
- 当前版本为浏览器端像素，不包含 Meta Conversions API、TikTok Events API、Google Enhanced Conversions 等服务器端回传。

## 网站功能

- WordPress + WooCommerce 原生主题，无 Elementor 依赖；购物车、结账及在线支付默认关闭。
- 工厂批发、零售和两者并行三种商品模式。
- 18 个草稿商品系列、58 个已核对视觉配置和 118 张目录媒体；每个系列包含独立介绍、特点、关键词和图片映射。
- 英语、西班牙语、葡萄牙语（巴西）的主题与插件语言包，以及 36 行西班牙语/葡萄牙语商品翻译稿。
- Polylang 语言菜单显示所有已配置语言，并在已关联译本存在时切换到对应页面。
- Facebook、TikTok、WhatsApp、Messenger 可配置入口；Telegram 可在后续填写链接启用。页眉默认 WhatsApp 为 `+852 9019 9249`。
- 五椅组合主视觉；公开首页已移除 `8011`，内部 SKU/来源字段保留以便追溯。
- 六张真实目录图与六个 3D 外观逐一匹配；选择图片会同步待加载模型，3D 仅在用户点击后加载。
- 响应式布局、滚动动画、减少动态效果支持、SEO 基础和 WooCommerce 商品页。
- 商品均为草稿，价格、币种、税务和库存留空，避免发布未经确认的信息。

### 图片与 3D 对应关系

| 真实产品图片 | 3D 外观 |
|---|---|
| Black / ivory | Black / ivory |
| Red / black with color trim | Red / black with color trim |
| Black / white with blue piping | Blue / white |
| Black / yellow | Yellow / black |
| Red / black shaped cushions | Red / black |
| Black / orange fabric | Orange / black |

## 验证结果

- 主题检查：81 项通过、0 项失败；1 项预期提示（询价处理由 Store Core 插件负责）
- 浏览器检查：96 / 96 通过（1440、1024、768、390、360、320 px，并覆盖页眉社交入口、四张工厂照片、放大查看、六组图片与 3D 映射）
- Store Core 插件检查：48 / 48 通过
- 广告追踪专项检查：12 / 12 通过
- 多语言检查：22 / 22 通过；主题 ES/PT 各 258 / 258，插件 ES/PT 各 109 / 109
- PHP AST 语法解析：31 / 31 文件通过
- 发布包检查：41 / 41 通过；ZIP 完整性、来源一致性、可复现构建和 SHA-256 已验证

[查看完整验证报告](WORDPRESS-VALIDATION.md) · [查看发布清单](release-manifest.json) · [查看校验值](SHA256SUMS.txt)

工厂版块已使用四张真实生产现场照片和真实成品仓库视频，并提升为主视觉后的第一内容版块；旧版三张 AI 工厂示意图已从主题包中移除。
