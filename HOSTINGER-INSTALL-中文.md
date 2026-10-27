# XIUJIN 在 Hostinger 的安装顺序

本网站使用 WordPress 和 WooCommerce 管理商品，但采用**询价目录模式**，不启用在线付款。

## 1. 基础插件

1. 在 WordPress 后台进入 **插件 → 安装插件**。
2. 安装并启用作者为 **Automattic** 的 **WooCommerce**。
3. 跳过 WooCommerce 的付款、税务和配送设置；不要安装 Stripe、PayPal 或其他支付网关。

## 2. 上传 XIUJIN 主题

1. 进入 **外观 → 主题 → 安装主题 → 上传主题**。
2. 上传 `XIUJIN-WordPress-Theme-1.2.1.zip`。
3. 安装完成后启用 **XIUJIN Furniture**。

## 3. 上传询价功能插件

1. 进入 **插件 → 安装插件 → 上传插件**。
2. 上传 `XIUJIN-Store-Core-1.2.1.zip` 并启用。
3. 网站会使用商品展示与询价流程，购物车、结账和付款入口不会作为客户购买路径。

## 4. 导入商品

1. 解压 `XIUJIN-WooCommerce-Import-18-Series-58-Configurations.zip`。
2. 按包内 `README-导入说明.md` 上传图片并导入草稿商品 CSV。
3. 商品保持草稿，逐款核对价格、MOQ、交期、材料、颜色、库存和运输条件后再发布。

## 5. 多语言和社媒

- 安装 Polylang 或 WPML 后，可建立英语、西班牙语和葡萄牙语页面；主题与插件固定界面已有三语语言包。
- 在 **外观 → 自定义** 中填写 Facebook、Instagram、TikTok、WhatsApp 和 Messenger 链接。
- WhatsApp 和 Messenger 可作为主要询价入口。

## 6. 广告像素与询盘回传

Store Core 可以在访客同意后加载 Google Ads、Meta Pixel 和 TikTok Pixel，并在**WordPress 邮件程序接受询盘邮件发送**后回传一次 Lead 事件。所有 ID 默认为空，空值平台不会加载任何第三方脚本。

### 6.1 准备平台 ID

1. **Google Ads**：进入 Google Ads 的 **目标 → 转化 → 摘要**，新建“网站”来源的“提交潜在客户表单”转化操作。在“使用 Google 标签”的安装信息中记录转化 ID（格式 `AW-123456789`）和转化标签。
2. **Meta**：进入 Meta Events Manager，选择 **Connect data → Web → Meta Pixel** 创建数据源，记录纯数字的 Pixel ID。
3. **TikTok**：进入 TikTok Ads Manager 的 **Tools → Events Manager → Web Events**，创建 Pixel 并选择手动安装，记录 Pixel ID。
4. **GA4（可选）**：只有网站尚未通过 Site Kit、Google Tag Manager 或其他插件加载 GA4 时，才填入格式为 `G-XXXXXXXXXX` 的 Measurement ID。已由 Site Kit 输出 GA4 时保持此项为空，避免页面浏览被统计两次。

各平台后台的菜单名称可能随账户语言或界面更新而略有变化。不要将广告账户编号、商务管理平台编号或活动编号当作像素 ID。

### 6.2 在 WordPress 中填写

1. 进入 **设置 → XIUJIN Tracking**。
2. 将已获得的 Google Ads 转化 ID 与转化标签、Meta Pixel ID 和 TikTok Pixel ID 填入对应字段。
3. 未开通的平台保持为空；不要填写示例值或猜测的 ID。
4. 保存后清除 LiteSpeed/Hostinger 页面缓存和 CDN 缓存。
5. 确认其他插件、主题、Site Kit 或 Google Tag Manager 没有再次注入相同的 Google Ads、Meta 或 TikTok ID。

> 重要：此同意面板只能控制 Store Core 自己加载的标签，不能撤回 Site Kit、MonsterInsights、Google Tag Manager 或其他插件已经发出的请求。你当前网站装有 Site Kit；如果要求访客同意前全站不连接分析/广告平台，请在 Site Kit 中关闭 Analytics 前端输出（Search Console 可继续使用），并停用其他重复标签，或改由一个统一的 CMP 管理全部标签。若保留 Site Kit 的 GA4，下面的 GA4 字段必须留空。

### 6.3 验证同意与询盘事件

1. 使用无痕窗口访问前台。未选择同意时，Google、Meta 和 TikTok 脚本不应发起网络请求。
2. 点击“仅必要功能”后，广告脚本仍不应加载；点击“接受分析和广告”后，才会加载已配置平台。
3. 提交一次真实测试询盘，确认收件邮箱已收到邮件。只有 `wp_mail` 成功后，网站才会在已同意的浏览器中发送一次 Lead/SubmitForm 事件。
4. 分别用 Google Tag Assistant、Meta Pixel Helper 和 TikTok Pixel Helper 确认页面事件和询盘事件只出现一次。广告平台后台可能需要数小时才显示诊断数据。
5. 在 WordPress **设置 → 隐私**中审核并发布隐私政策，说明使用的广告平台、同意选择和保留期。

此版为浏览器端像素与 Google Ads 询盘转化回传，不包含 Meta Conversions API、TikTok Events API 或 Google Enhanced Conversions 的服务器端回传。这些功能需要单独的访问令牌、域名验证、隐私设置与服务器端部署。

## 7. 上线前

- 连接正式域名并启用 HTTPS。
- 设置询价接收邮箱并测试邮件送达。
- 替换示意性工厂场景图后，再将其描述为真实工厂照片。
- 删除未使用的示例文章、页面和不需要的预装插件。
