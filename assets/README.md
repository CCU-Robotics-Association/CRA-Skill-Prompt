# 文档配套资源

将实际使用的 SVG 复制到目标仓库，保持与 Markdown 引用相对应的路径。README 位于仓库根目录时，可以使用 `./assets/icons/book-open.svg`；文档位于子目录时，应同步调整路径或复制资源到该目录。

## 来源与许可

- `icons/*.svg` 来源于 [Lucide](https://github.com/lucide-icons/lucide/tree/main/icons)，描边统一为紫色 `#8B5CF6`，保留原始线条与比例。复制图标时保留 [icons/LICENSE](./icons/LICENSE) 及 [icons/README.md](./icons/README.md)
- `matlab-badge.svg` 的 Logo 来源于 [Devicon MATLAB](https://github.com/devicons/devicon/blob/master/icons/matlab/matlab-original.svg)，保留原始图形与渐变，许可见 [LICENSE.devicon](./LICENSE.devicon)
- `python-badge.svg` 内嵌 [Python 官方 Logo](https://www.python.org/community/logos/)，保留黄蓝双色图形与渐变；官方使用说明见该页面。徽章背景为 `#2F4C6C`，文字为白色

Python 与 MATLAB 徽章均为 20px 高的独立 SVG，图标已内嵌。直接引用 SVG 文件可以避免将复杂 Logo 编码进远程 URL 后出现 `URI Too Long`。

以上第三方许可文件仅对应所标明的资源，不代表整个仓库采用相同许可证。
