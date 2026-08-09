# 个人主页双栏布局更新

此包包含 3 个文件，保持原有个人信息、Experience、News、论文和链接不变，只重组首页布局。

## 效果

- 桌面端：照片、个人介绍和 Experience 完全固定。
- 左下 News 是独立滚动区；右侧论文是另一个独立滚动区。
- 已删除左下角全部社交图标。
- 已压缩导航栏下方空白，让主页内容整体上移。
- 个人正文、Experience、News、论文标题、作者和期刊统一使用同一正文基准字号。
- Experience、News 和 Publications 的区块标题统一为同一级字号。
- 每篇论文都显示一个 160 × 100 像素的图片占位。
- 后续真实图片会统一用 `object-fit: cover` 居中裁剪为 160 × 100，不会因原图比例不同而改变版式。
- 900px 以下自动恢复单列整页滚动；520px 以下论文图像排列在文字上方。

## 文件

- `_layouts/about.liquid`：新的首页双栏结构。
- `_sass/_home.scss`：首页布局、字号、滚动区和论文图片规则。
- `assets/css/main.scss`：增加 `@use "home";` 以载入首页样式。

将这三个文件按原目录覆盖到仓库的 `main` 分支即可。推送后 GitHub Actions 会重新部署主页。

## 验证

已完成：

- Liquid 文件使用仓库指定的 Shopify Prettier 插件格式化。
- SCSS 文件通过 Dart Sass 编译。
- `homepage-layout-preview.html` 已使用线上真实主页内容更新。