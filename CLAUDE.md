# 娃哈哈AD钙奶H5互动页

单文件自包含HTML互动页「童心检测中心·天选AD人」，大广赛参赛作品。

## 技术栈
- 单文件HTML（Base64内嵌图片+音频）
- Google Fonts: ZCOOL KuaiLe / QingKe HuangYou / Press Start 2P / Long Cang
- html2canvas CDN（截图分享）
- 纯CSS动画 + 原生JS

## 关键规则
- **不新增外部依赖**：保持单文件可离线分享
- **音频Base64内嵌**：首次静音播放绕过浏览器自动拦截
- **字体**使用已配置的preconnect，不新增Google Fonts家族
- **配色**使用CSS变量 `--ad-green`, `--ad-red`, `--gold` 等
- **响应式**：容器 `max-width: 480px` 移动端优先，字号用 `clamp()` 流体缩放
- **截图**：html2canvas 2.5x scale，不替换为其他截图方案

## 响应式断点
| 断点 | 覆盖设备 |
|------|---------|
| ≤350px | 极端小屏 |
| ≤374px | iPhone SE / 小屏Android |
| 375-414px | 主流中屏过渡 |
| ≥415px | 大屏手机/平板 |

## 部署
- **GitHub Pages**: gh-pages分支
- **Cloudflare Pages**: workers.dev 自动部署
- **推送**: `gh` CLI
