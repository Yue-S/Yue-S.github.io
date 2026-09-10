# Zijun Wang · Personal

个人主页：<https://yue-s.github.io>。使用 [Moonwalk](https://github.com/abhinavs/moonwalk) 主题，保留浅色首页、深浅色切换、项目卡片和博客。

## 修改内容

- `_config.yml`：姓名、介绍、主题开关。
- `_data/home.yml`：导航、项目卡片、页脚链接。
- `about.md`：个人简介。
- `_posts/YYYY-MM-DD-title.md`：文章，文件头添加 `layout: post` 和 `title`。
- `_sass/custom.scss`：本地样式调整。

目前没有导入虚构的个人经历或模板示例文章。首页会在添加第一篇文章后显示文章列表。

## 本地预览

安装 Ruby 3.3 和 Bundler，然后在仓库目录运行：

```sh
bundle install
bundle exec jekyll serve
```

浏览器访问 <http://localhost:4000>。

## GitHub Pages

1. 将修改合并并推送至 `master` 分支。
2. 仓库 **Settings → Pages → Build and deployment → Source** 选择 **GitHub Actions**。
3. `Build and deploy GitHub Pages` 工作流会构建并发布。也可以在 Actions 页手动运行。

主题使用现代 Sass，需要 Jekyll 4 构建，因此使用上面的 Actions 工作流。
Pull request 仅构建验证，不发布。

## 旧站点与主题来源

- 原 Academic Pages 源码和示例内容保存在 `_legacy/`，不参与网站构建；原 `images/`、`files/` 也保留但暂不发布。引用其中素材时，从 `_config.yml` 的 `exclude` 列表移除对应目录。
- Moonwalk 源码来自 `abhinavs/moonwalk`，版本 `abab9f3`（2026-05-05），已复制到仓库，不依赖构建时拉取主题。
- 保留 Moonwalk 的 MIT 许可证；旧主题许可证在 `_legacy/LICENSE`。
- 使用 `jekyll-seo-tag`，未启用 Soopr 等第三方分享或统计服务。
