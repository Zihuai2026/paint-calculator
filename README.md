# Paint Calculator · 家装油漆用量计算器

一个纯静态的单页工具网站：输入房间尺寸，实时计算墙面面积与所需油漆加仑数（含涂刷遍数建议、墙面展开线框图、一键复制、付费 PDF 占位、Amazon 联盟商品位）。

## 功能

- 📐 输入房间长/宽/高（英尺）+ 门窗总面积，实时计算
- 🧮 公式：`墙面面积 = 2 × (长 + 宽) × 高 − 门窗面积`，`加仑数 = 墙面面积 × 遍数 ÷ 400`（向上取整）
- 🖼️ SVG 四面墙展开线框图，尺寸变化即时重绘
- 📋 一键复制计算结果（含 Toast 提示，带剪贴板降级方案）
- 💳 「下载采购清单 PDF」付费弹窗（Stripe Payment Link 占位）
- 🛒 底部 Amazon 联盟商品卡 ×3
- 🔍 SEO：meta 描述 / Open Graph / FAQ 结构化数据（JSON-LD）

## 本地使用

无任何依赖，直接用浏览器打开 `index.html`，或用 HBuilderX / VS Code 打开编辑。

## 上线（GitHub Pages）

```bash
git init
git add .
git commit -m "init: paint calculator"
git remote add origin https://github.com/<你的用户名>/paint-calculator.git
git push -u origin main
```

然后在 GitHub 仓库 **Settings → Pages → Deploy from a branch → main /root** 即可。

## 上线前待办（变现闭环）

- [ ] 替换 `index.html` 中所有 `https://example.com/paint-calculator/` 为真实域名
- [ ] Amazon 联盟：3 个商品卡 `href="#"` 换成带追踪 ID 的联盟链接
- [ ] Stripe：创建 Payment Link，替换付费弹窗中 `btnPay` 的占位逻辑
- [ ] 目标用户为海外时，制作英文版本（`lang="en"`）并提交 Google Search Console
