# XIUJIN WordPress + WooCommerce 网站

这是为 **Bazhou Xiujin Furniture Co., Ltd / XIUJIN** 制作的 WordPress 网站，面向办公椅、电竞椅和行政办公椅的工厂批发与零售询价。

![XIUJIN WordPress 首页预览](XIUJIN-WordPress-preview-desktop.png)

## 现在安装哪个文件

在 WordPress 后台进入 **外观 → 主题 → 安装主题 → 上传主题**，只上传：

- [`XIUJIN-WordPress-Theme-1.1.0.zip`](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-Theme-1.1.0.zip)

`XIUJIN-WordPress-Complete-1.1.0.zip` 是供电脑解压的完整交付合集，不能在“上传主题”页面安装。

## 下载文件

- [WordPress 主题 1.1.0](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-Theme-1.1.0.zip)
- [询价功能插件 1.1.0](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-Store-Core-1.1.0.zip)
- [WooCommerce 商品导入包：18 个系列、58 个配置、118 张媒体](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WooCommerce-Import-18-Series-58-Configurations.zip)
- [完整交付包：主题、插件、商品包、报告和预览](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-Complete-1.1.0.zip)
- [可复现构建源码](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-Source-1.1.0.zip)
- [本地交互预览](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-Preview.zip)
- [手机端预览图](https://github.com/chunboye7-tech/tt/raw/refs/heads/main/XIUJIN-WordPress-preview-mobile.png)

详细步骤见 [Hostinger 安装说明](HOSTINGER-INSTALL-中文.md)，文件用途见 [先从这里开始](START-HERE-中文.md)。

## 当前版本

- WordPress + WooCommerce 原生主题，无 Elementor 依赖。
- WooCommerce 用于商品和目录管理；购物车、结账及在线支付默认关闭。
- 工厂批发、零售和两者并行三种商品模式。
- 18 个草稿商品系列、58 个已核对视觉配置和 118 张目录媒体；每个系列包含独立介绍、特点、关键词和图片映射。
- 英语、西班牙语、葡萄牙语（巴西）的主题与插件语言包，以及 36 行西班牙语/葡萄牙语商品翻译稿。
- Facebook、Instagram、TikTok、WhatsApp、Messenger 可配置入口；默认 WhatsApp 已更新为 `+86 184 0684 5852`。
- 五椅组合主视觉；公开首页已移除 `8011`，内部 SKU/来源字段保留以便追溯。
- 六张真实目录图与六个 3D 外观逐一匹配；选择图片会立即同步待加载模型，3D 仅在用户点击后加载。
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

- 主题检查：80 项通过、0 项失败；1 项预期提示（询价处理由 Store Core 插件负责）
- 浏览器检查：84 / 84 通过（1440、768、390、320 px，并覆盖六组图片与 3D 映射）
- Store Core 插件检查：35 / 35 通过
- 多语言检查：22 / 22 通过；主题 ES/PT 各 240 / 240，插件 ES/PT 各 77 / 77
- PHP AST 语法解析：30 / 30 文件通过
- 发布包检查：40 / 40 通过；ZIP 完整性和 SHA-256 已验证

[查看浏览器验证报告](WORDPRESS-VALIDATION.md) · [查看发布清单](release-manifest.json) · [查看校验值](SHA256SUMS.txt)

工厂场景图目前是明确标注的设计示意图，获得真实工厂照片后可在 WordPress 中替换。
