# vimact-site

VimAct 官网的构建产物仓库。这里的文件全部由 `pnpm site:deploy` 从 VimAct 源码仓库生成后推送，不要手工编辑，任何手工改动都会在下一次部署时被覆盖。

当前可访问地址：<https://adam-ikari.github.io/vimact-site/>（preview 档，站点挂在 `/vimact-site/` 路径下）
目标地址：<https://vimact.is-a.dev>，域名注册下来、站点切到 prod 档之后才生效。

- 站点源码与内容：VimAct 私有仓库的 `website/` 目录，暂不公开。
- 需要修改文案，改源码仓库后重新部署。
- APK 发布物放在本仓库的 [Releases](https://github.com/adam-ikari/vimact-site/releases)。

## 仓库内容

`.nojekyll` 关掉 Pages 的 Jekyll 处理，避免下划线前缀的目录被丢弃。`CNAME` 和 `robots.txt` 只在 prod 档出现：部署脚本把它们写进产物，Pages 据此把仓库绑到 `vimact.is-a.dev`，同时产出 `sitemap.xml`，`robots.txt` 放行整站并把 sitemap 交给爬虫。preview 档三样都没有，靠每个页面 `<head>` 里的 `noindex` 挡住收录（路径型预览读不到站点根的 robots.txt），其余是 VitePress 输出的静态站点。
