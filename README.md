# vimact-site

VimAct 官网的构建产物仓库。这里的文件全部由 `pnpm site:deploy` 从 VimAct 源码仓库生成后推送，不要手工编辑，任何手工改动都会在下一次部署时被覆盖。

线上地址：<https://vimact.is-a.dev>

- 站点源码与内容：VimAct 私有仓库的 `website/` 目录，暂不公开。
- 需要修改文案，改源码仓库后重新部署。
- APK 发布物放在本仓库的 [Releases](https://github.com/adam-ikari/vimact-site/releases)。

## 仓库内容

`CNAME` 把 GitHub Pages 绑到 `vimact.is-a.dev`；`.nojekyll` 关掉 Pages 的 Jekyll 处理，避免下划线前缀的目录被丢弃。除此之外是 VitePress 输出的静态站点。
