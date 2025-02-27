---
title: "基于Jekyll-contrast和Giscus搭建Github Pages"
layout: post
---

1. fork [niklasbuschmann/contrast](https://github.com/niklasbuschmann/contrast), 仓库名称设置为 `[username].github.io`
2. `Setting - General - Features` 启用 `Discussions`
3. `Setting - Pages - Build and deployment - Source` 改为 `Github Actions`
4. `Setting - Pages - Jekyll` 点击 `Configure`, 再点击 `Commit Changes`, 在 `Actions` 页面点击 `Run Workflow`
5. [Github Apps - giscus](https://github.com/apps/giscus/), 安装 `giscus`
6. [giscus](https://giscus.app/), `仓库` 填入 `[username].github.io`, `Discussion 分类` 选择 `General`, 得到 `启用 giscus` 的信息
7. `./_config.yml` 自定义修改, `comments` 改为 `giscus`, 并根据格式写入 `启用 giscus` 的信息
8. `_layouts\default.html` 在 `discus` 下方粘贴 `启用 giscus` 的信息
9. `_layouts\post.html` 在 `discus` 下方, 加一个`<div></div>`, 粘贴 `启用 giscus` 的信息
