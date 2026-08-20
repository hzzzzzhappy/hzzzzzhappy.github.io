# 个人主页双栏与论文分类更新

## 论文分类

主页右侧不再显示 “Some publications” 或 “Some working papers”，改成两个研究方向：

- **Real-World Computer Vision**：现有异常检测、工业检测与空间视觉论文。
- **Precision Medicine**：现有 CONTEXTOR，以及未来的精准医疗论文。

当前归类结果：

- Real-World Computer Vision：8 篇已发表论文 + 2 篇 Working Papers。
- Precision Medicine：1 篇已发表论文（CONTEXTOR）。
- Working Papers 仍不显示图片、占位框或空白图片列。

以后新增或移动论文时，在 _bibliography/papers.bib 的对应条目中维护：

    selected={true},
    research_area={real_world_cv},
    status={published}

精准医疗论文使用：

    research_area={precision_medicine}

Working Paper 使用：

    status={working}

可用值：

- research_area={real_world_cv}
- research_area={precision_medicine}
- status={published}
- status={working}

## 布局效果

- 桌面端：照片、个人介绍和 Experience 完全固定。
- 左下 News 独立滚动；右侧论文独立滚动。
- 左下角社交图标已删除，导航栏下方空白已压缩。
- 正文、Experience、News、论文标题、作者和期刊使用统一正文基准字号。
- 页面背景为纯白色。
- 900px 以下恢复单列整页滚动。

## 论文图片

9 张原图统一采用接近原图中位比例的 5:3 显示：

- 显示尺寸：180 × 108 像素。
- 裁剪方式：object-fit: cover，居中裁剪。
- 不拉伸、不改变原始图片文件。
- Working Papers 不显示图片。

## 需要覆盖的文件

- _layouts/about.liquid：首页双栏结构与分类入口。
- _includes/home_papers_by_topic.liquid：两个研究方向的论文筛选规则。
- _sass/_home.scss：布局、滚动、统一字号、图片及 Working Papers 无图规则。
- assets/css/main.scss：载入首页样式。
- _bibliography/papers.bib：论文图片、研究方向和发表状态字段。
- assets/img/publication_preview/：9 张原始论文图片。

将源码包中的文件按原目录覆盖到 GitHub 仓库的 main 分支即可。

## 验证结果

- Liquid 已按仓库规范格式化。
- SCSS 已通过 Dart Sass 编译。
- 已验证分类标题为 Real-World Computer Vision 和 Precision Medicine。
- 已验证旧的 Some publications / Some working papers 标题均不存在。
- 已验证 9 篇有图论文显示 9 张图片。
- 已验证 2 篇 Working Papers 均不显示图片。
