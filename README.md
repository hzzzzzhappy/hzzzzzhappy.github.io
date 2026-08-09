# 个人主页双栏布局更新

## 布局效果

- 桌面端：照片、个人介绍和 Experience 完全固定。
- 左下 News 独立滚动；右侧论文独立滚动。
- 左下角社交图标已删除，导航栏下方空白已压缩。
- 正文、Experience、News、论文标题、作者和期刊统一使用同一正文基准字号。
- Working Papers 不显示图片、占位框或空白图片列。
- 900px 以下恢复单列整页滚动。

## 论文图片

根据 9 张原图的宽高比，中位比例约为 1.636，因此统一采用接近中位值的 5:3：

- 显示尺寸：180 × 108 像素。
- 裁剪方式：`object-fit: cover`，居中裁剪。
- 不拉伸、不改变原始图片文件。
- 未提供图片的已发表论文会继续显示 IMAGE 占位框。

对应关系：

- IEC3D-AD → `IEC3D-AD.png`
- MVFM-3DAD → `MVFM-3DAD.jpg`
- Information-aware Reconstruction / IRM3D-AD → `IRM3D-AD.png`
- BinaryAD → `BinaryAD.png`
- Multi-scale Feature Fusion / MFF-M3AD → `MFF.png`
- Lightweight Rotationally Invariant Features → `rif.png`
- CONTEXTOR → `contextor.png`
- Taming Anomalies → `taming.png`
- Look Inside for More / AAAI → `AAAI.png`

## 文件

- `_layouts/about.liquid`：首页双栏结构。
- `_sass/_home.scss`：布局、滚动、统一字号与 5:3 图片规则。
- `assets/css/main.scss`：载入首页样式。
- `_bibliography/papers.bib`：9 篇论文的 `preview` 字段。
- `assets/img/publication_preview/`：9 张原始论文图片。

将这些文件按原目录覆盖到仓库的 `main` 分支即可。

## 验证

- Liquid 已按仓库规范格式化。
- SCSS 已通过 Dart Sass 编译。
- 已验证 9 篇已发表论文显示 9 张图片。
- 已验证 2 篇 Working Papers 均不显示图片。
- Edge 预览为静态双栏 HTML，不依赖浏览器运行时重排。