# MyWiki Project

个人维基站点，样式来自 **notebook** 目录（al-folio 主题）。

## 已应用的样式与结构

- **_sass/**：SCSS 变量、主题、布局、排版、导航栏、页脚、博客等样式
- **assets/css/**：主样式表 `main.scss` 及 Bootstrap、MDB、代码高亮等静态 CSS
- **assets/js/**：主题切换、Masonry、搜索等前端脚本
- **_layouts/** 与 **_includes/**：页面布局与公共片段（头部、页脚、脚本等）
- **_config.yml**：站点配置（已精简，保留 al-folio 所需项）
- **_pages/about.md**：首页（permalink: /），使用与 notebook 相同的 about 布局

## 本地构建

```bash
bundle install
bundle exec jekyll serve
```

访问 http://localhost:4000 查看效果。

## 部署到 GitHub Pages

推送至 `main` 分支后，`.github/workflows/jekyll-gh-pages.yml` 会自动构建并部署。

请在 `_config.yml` 中修改 `url` 为你的 GitHub Pages 地址（例如 `https://你的用户名.github.io`），若使用项目页则设置 `baseurl: /mywiki`。

## 添加新页面

在 `_pages/` 下新建 Markdown 文件，设置 front matter，例如：

```yaml
---
layout: page
title: 页面标题
permalink: /your-page/
---
```

内容写在下方的 Markdown 中即可。
