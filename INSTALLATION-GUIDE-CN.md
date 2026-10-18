# XIUJIN Shopify 新主题安装与使用说明

本主题根据用户提供的 XIUJIN Facebook 视觉制作，采用深蓝、金色和白色。公司名与电话来自截图：Bazhou Xiujin Furniture Co., Ltd、+852 9019 9249，发布前请再核对；电话没有被自动设为 WhatsApp。

## 交付文件

- `XIUJIN-Shopify-Theme-DRAFT.zip`：可直接上传的 Online Store 2.0 主题。
- `XIUJIN-Store-Preview.zip`：本地静态预览；其中表单不会发送。
- `XIUJIN-products-DRAFT.csv`：18 个产品系列，全部为 draft / Published=FALSE；每款有独立标题、描述、卖点、标签和 SEO 文案。
- `XIUJIN-58-visual-configurations.csv`：18 个系列与 58 个外观配置的对应表。
- `XIUJIN-58-product-images.zip`：58 张已核对且不重复的产品图片，包括第 171 行粉、灰、米色三款。
- `椅子B2B上架整理草稿.xlsx`：内部核对表，不适合直接公开。

## 替换主题

1. Shopify 后台 → 在线商店 → 主题 → Import／导入主题 → Upload zip file。
2. 上传 `XIUJIN-Shopify-Theme-DRAFT.zip`。它会成为一个新的草稿主题；旧主题不会自动覆盖。
3. 先点 Preview 预览。确认后再 Publish。发布会替换当前在线主题，所以请保留旧主题用于回退。
4. 主题编辑器 → Theme settings → Brand and contact：上传原始 Logo，核对公司名、电话和邮箱，填入真实 Facebook、Instagram、TikTok、WhatsApp、Messenger 链接。

## 首页内容

首页已包含 10 张用户提供的主页图、3 张工厂流程插画、18 个产品系列、交互式 3D 椅子、询价表单和轻量滚动动画。工厂图默认保留“插画”说明；拿到真实工厂照片后，在 Factory and supply 区块逐张替换，再关闭说明。

主题支持批发和零售。默认 `product.json` 为批发询价；将某商品的 Theme template 指定为 `product.retail`，并填写真实价格、币种、库存与运费后，才启用 Add to cart。购物车入口默认显示。批量采购仍可使用询价表单。

## 产品导入

CSV 按原表表头“变化款（相同产品参数 价格）”整理为 18 个父产品系列，并另交付 58 个外观配置及图片。因为原表价格币种不明，CSV 不写价格、库存、颜色元字段或认证。导入后按 58 款对应表逐款上传媒体并建立真实变体；不要把图片名称自动当作颜色值。

所有缺正式型号的商品使用 `source-row-*` 内部标签和稳定 handle。第 171 行遗漏款已经补入。PVC／PU没有描述为真皮；承重、认证、产能、交期、MOQ、箱规和装柜量在没有证据时没有对外承诺。

## 英文、西班牙语、葡萄牙语

主题含 `en`、`es`、`pt-BR`、`pt-PT` 语言文件，固定界面、购物车、产品操作、询价表单和 3D 控件已接入翻译。Shopify 后台 → Settings → Languages／Markets 中发布需要的语言，语言选择器才会出现。首页可编辑文案、菜单、产品标题、产品描述、SEO、图片 alt 和政策内容需要用 Shopify Translate & Adapt 翻译；主题代码不能自动翻译商家录入的内容。

## 询价、SEO 与社媒

询价使用 Shopify 原生 contact 表单，不需要 Flow。上线前在在线主题里提交一次测试，并确认店铺通知邮箱实际收到全部字段。主题包含 canonical、动态 meta、Open Graph、Twitter Card、Organization / WebSite / Product JSON-LD、合理标题层级和搜索／购物车 noindex。多语言 hreflang 由 Shopify Markets 依据已发布语言与域名生成，上线后在页面源代码中检查一次，避免重复输出。

社媒链接只在 Theme settings 填写后显示；请使用完整 `https://` 链接。WhatsApp 通常使用 `https://wa.me/国家码手机号`，Messenger 通常使用 `https://m.me/主页用户名`。

## 已验证与仍需在线核对

当前环境已检查主题结构、Liquid／schema、JSON、JavaScript、ZIP 完整性、320–1440px 页面宽度、图片加载、菜单、画廊、3D 切换、询价必填项与 reduced-motion。Shopify 真实导入、支付、税费、运费、邮件送达、Markets 语言域名和真实社媒链接仍需在店铺后台核对。
