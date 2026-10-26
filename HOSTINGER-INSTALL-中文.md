# XIUJIN 在 Hostinger 的安装顺序

本网站使用 WordPress 和 WooCommerce 管理商品，但采用**询价目录模式**，不启用在线付款。

## 1. 基础插件

1. 在 WordPress 后台进入 **插件 → 安装插件**。
2. 安装并启用作者为 **Automattic** 的 **WooCommerce**。
3. 跳过 WooCommerce 的付款、税务和配送设置；不要安装 Stripe、PayPal 或其他支付网关。

## 2. 上传 XIUJIN 主题

1. 进入 **外观 → 主题 → 安装主题 → 上传主题**。
2. 上传 `XIUJIN-WordPress-Theme-1.1.0.zip`。
3. 安装完成后启用 **XIUJIN Furniture**。

## 3. 上传询价功能插件

1. 进入 **插件 → 安装插件 → 上传插件**。
2. 上传 `XIUJIN-Store-Core-1.1.0.zip` 并启用。
3. 网站会使用商品展示与询价流程，购物车、结账和付款入口不会作为客户购买路径。

## 4. 导入商品

1. 解压 `XIUJIN-WooCommerce-Import-18-Series-58-Configurations.zip`。
2. 按包内 `README-导入说明.md` 上传图片并导入草稿商品 CSV。
3. 商品保持草稿，逐款核对价格、MOQ、交期、材料、颜色、库存和运输条件后再发布。

## 5. 多语言和社媒

- 安装 Polylang 或 WPML 后，可建立英语、西班牙语和葡萄牙语页面；主题与插件固定界面已有三语语言包。
- 在 Polylang 中添加 `English (en_US)`、`Español (es_ES)` 和 `Português (pt_BR)`。主题会显示所有已配置语言；访问 `/es/` 与 `/pt/` 时会加载内置固定界面翻译。
- 页面、商品、菜单和自定义器中手工保存的内容仍需在 Polylang 中分别建立翻译。
- 在 **外观 → 自定义** 中填写 Facebook、Instagram、TikTok、WhatsApp 和 Messenger 链接。
- WhatsApp 和 Messenger 可作为主要询价入口。

## 6. 上线前

- 连接正式域名并启用 HTTPS。
- 设置询价接收邮箱并测试邮件送达。
- 替换示意性工厂场景图后，再将其描述为真实工厂照片。
- 删除未使用的示例文章、页面和不需要的预装插件。
