<!--
作者 / Author: XCrane
-->

# CRA README 编写 Prompt

请根据我提供的资料，为 CCU Robotics Association 编写或修改 README.md。以我提供的最新版 README 为格式参考，保持协会统一的标志、徽章和文档排版。正文以中文为主，搭配简洁的英文标题，使用 SVG 图标。

## 使用方式

将本文完整提供给 AI，并附上目标仓库资料、现有文档及本次修改要求。同目录下的 [README_EXAMPLE.md](./README_EXAMPLE.md) 是可直接预览的结构参考；它展示本 Prompt 的排版，不代表目标仓库的事实。使用本地图标时，将所需的 `assets/` 资源一同提供或复制到目标目录。

以下填写表可与 Prompt 一起提交。未提供的信息先检查目标仓库，仍无法确认的必需信息使用清晰的占位文字；非必需章节省略。不要编造年份、作者、许可证或链接。

```text
任务：新建 / 修改 README.md（或明确指定的其他 Markdown 文档）
目标文件：
文档主题与用途：
仓库及资料地址：
现有文档与参考文件：
文档作者（可选，已有作者优先保留）：
起始年份（以资料为准）：
已声明的许可证（未声明则不添加 License 徽章）：
需要保留的徽章、入口与内容：
本次新增或修改要求：
```

## 输入信息

- 文档作者：优先使用我指定的信息，其次保留目标文档已有作者；均未提供时默认 `XCrane`。多位作者使用顿号 `、` 连接。
- 文档主题：根据当前仓库或目录的用途确定。
- 英文副标题：与中文主题含义对应，使用自然、准确、简练的英文。
- 起始年份：沿用已有文档或我提供的年份，不自行推断。
- 仓库地址、目录地址、内容和贡献者信息：以提供的资料为准。
- 如果我提供现有 README，先阅读并保留其中有效的信息与手动调整，再进行修改。

## 参考与修改原则

- 每次修改前，重新阅读本次提供的 README，以文件中的最新内容和我的最新要求为准。
- 我的最新明确要求优先于以下默认规则；强制使用协会徽章、移除 `AREA ROBOTICS` 的要求优先于保留旧徽章。
- 除我明确要求修改或上述强制要求外，保留现有徽章的位置、顺序、换行分组、配色、Logo 和链接。徽章始终位于页首的年份说明之后、导航之前，不移至正文或折叠区域；补充协会徽章时不改变其他徽章的相对顺序和分组。
- 将示例中的格式提炼为规则，作者名单、起始年份、许可证、技术栈等具体事实仍取自目标仓库或我提供的资料。
- 我仅要求更新 Prompt 时，只修改 Prompt。

## 页首结构

严格按照以下顺序编排：

1. 文件第一行必须是 HTML 注释，用于记录文档作者。作者信息只在源码中可见，不在预览中显示。按“输入信息”中的优先级确定作者，例如：

   ```html
   <!--
   作者 / Author: XCrane
   -->
   ```

   多作者时仅将作者行改为 `作者 / Author: XCrane、Bukaili`，姓名以实际资料为准。

2. 作者注释后空一行，使用 `<div align="center">` 包裹整个页首区域。

3. 首先放置协会官方透明 SVG Logo，链接到协会 GitHub 主页。保持 `width="132"`，保留 SVG 原始比例，不添加背景色，不改用头像或 PNG。使用以下代码：

   ```html
   <a href="https://github.com/CCU-Robotics-Association">
     <img src="https://raw.githubusercontent.com/CCU-Robotics-Association/.github/main/profile/assets/logo.svg" width="132" alt="CCU Robotics Association Logo">
   </a>
   ```

4. Logo 下方使用固定一级标题：

   ```markdown
   # CCU Robotics Association
   ```

5. 使用三级标题说明当前文档的主题，格式为 `### 中文主题 · English Title`。例如 `### CCU 机器人协会 · CCU Robotics Association`。保留已有副标题的措辞，英文大小写与术语在全文保持一致。

6. 单独一行写协会名称与时间范围，格式为 `CCU 机器人协会 · 起始年份 —— Future`。例如 `CCU 机器人协会 · 2024 —— Future`。具体文件、活动和贡献记录中的实际年份仍按事实保留。

7. 在年份说明下方集中放置当前文档选定的徽章，统一使用 `style=flat-square` 和 20px 高度。编辑时保留既有徽章组合和分组；下列样式目录用于需要对应徽章的场景，不代表每份文档都要加入全套徽章：
   - 每份协会文档都必须在顶部徽章区域包含以下协会专属徽章，并链接至协会 GitHub 主页；原文缺少时必须补充。不要添加或保留 `AREA ROBOTICS` 徽章，也不要用它代替协会专属徽章。左侧为白色 SVG 标志与 CCU，背景为近黑色 #181717，右侧 Robotics Association 背景为深紫色 #4C1D95。官方 Logo 以 Base64 SVG 嵌入 logo 参数，保持 flat-square 样式：
     `https://img.shields.io/badge/CCU-Robotics_Association-4C1D95?style=flat-square&labelColor=181717&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB3aWR0aD0iNTAxIiBoZWlnaHQ9IjQ3MCIgdmlld0JveD0iMCAwIDUwMSA0NzAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI%2BCiAgPHBhdGggZD0iTSA4OSA5NSBMIDAgNDY5IEwgNDQyIDQ2OSBMIDQ1MCA0MTQgTCAzMTkgMjMwIEwgMjQxIDIzMCBMIDM2OCA0MTEgTCA3MyA0MTAgTCAxNDkgOTcgWiBNIDExMSAxIEwgOTkgNTMgTCA0NDQgNTMgTCA0NDQgNjYgTCA0MjggMTYxIEwgNDc3IDIyNSBMIDUwMCAwIFoiIGZpbGw9IndoaXRlIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiLz4KPC9zdmc%2BCg%3D%3D`
   - 资料目录以实际需要和当前示例选定的徽章为准；只有我明确需要或原文已经包含时，才保留额外的归档、格式、存储信息徽章。
   - Flasher 和 NAOqi 徽章统一使用白色 #FFFFFF 背景、黑色文字及 flat-square 样式，名称与实际版本号在同一段中显示，不拆成左侧名称、右侧版本的双段徽章。版本号必须以目标仓库实际文件或明确资料为准，不照抄以下示例：
     - Flasher：`https://img.shields.io/badge/Flasher_2.1.0.19-ffffff?style=flat-square`
     - NAOqi：`https://img.shields.io/badge/NAOqi_2.8.7.4-ffffff?style=flat-square`
   - PPTX :
     `https://img.shields.io/badge/PPTX-D24726?style=flat-square&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIGZpbGw9IiNmZmZmZmYiPjx0aXRsZT5NaWNyb3NvZnQgUG93ZXJQb2ludDwvdGl0bGU%2BPHBhdGggZD0iTTEzLjUgMS41cTEuNDUzIDAgMi43OTUuMzc1IDEuMzQyLjM3NSAyLjUwOCAxLjA2IDEuMTY2LjY4NiAyLjEyIDEuNjQxLjk1Ni45NTUgMS42NDEgMi4xMjEuNjg2IDEuMTY2IDEuMDYxIDIuNTA4UTI0IDEwLjU0NyAyNCAxMnEwIDEuNDUzLS4zNzUgMi43OTUtLjM3NSAxLjM0Mi0xLjA2IDIuNTA4LS42ODYgMS4xNjYtMS42NDEgMi4xMi0uOTU1Ljk1Ni0yLjEyMSAxLjY0MS0xLjE2Ni42ODYtMi41MDggMS4wNjEtMS4zNDIuMzc1LTIuNzk1LjM3NS0xLjI5IDAtMi41Mi0uMzA1LTEuMjMtLjMwNC0yLjMzNy0uODg0LTEuMTA4LS41OC0yLjA2My0xLjQxOC0uOTU1LS44MzgtMS42OTMtMS44OTNILjk5N3EtLjQxMSAwLS43MDQtLjI5M1QwIDE3LjAwNFY2Ljk5NnEwLS40MS4yOTMtLjcwM1QuOTk2IDZoMy44OXEuNzM5LTEuMDU1IDEuNjk0LTEuODkzLjk1NS0uODM3IDIuMDYzLTEuNDE4IDEuMTA3LS41OCAyLjMzNy0uODg0UTEyLjIxIDEuNSAxMy41IDEuNXptLjc1IDEuNTM1djguMjE1aDguMjE1cS0uMTQtMS42NC0uODI2LTMuMDc2LS42ODYtMS40MzYtMS43ODItMi41MzEtMS4wOTUtMS4wOTYtMi41MzctMS43ODItMS40NDEtLjY4NS0zLjA3LS44MjZ6bS01LjI2MiA3LjU3cTAtLjY4LS4yMjgtMS4xNjYtLjIyOS0uNDg2LS42MjctLjc5LS4zOTktLjMwNS0uOTM4LS40NDYtLjUzOS0uMTQtMS4xNzItLjE0SDIuODQ4djcuODYzaDEuODR2LTIuNzQySDUuOTNxLjU3NCAwIDEuMTE5LS4xN3QuOTc4LS40OTNxLjQzNC0uMzIyLjY5OC0uODAyLjI2My0uNDguMjYzLTEuMTE0ek0xMy41IDIxcTEuMTcyIDAgMi4yNjItLjI4N3QyLjA1Ni0uODJxLjk2Ny0uNTM0IDEuNzc2LTEuMjc4LjgwOC0uNzQ0IDEuNDE4LTEuNjY0LjYxLS45Mi45ODQtMS45ODYuMzc1LTEuMDY3LjQ2OS0yLjIyN2gtOS43MDNWMy4wMzVxLTEuNzM1LjE0LTMuMjcuOTA4VDYuNzk3IDZoNC4yMDdxLjQxIDAgLjcwMy4yOTN0LjI5My43MDN2MTAuMDA4cTAgLjQxLS4yOTMuNzAzdC0uNzAzLjI5M0g2Ljc5N3EuNjQ0LjcxNSAxLjQxMiAxLjI3MS43NjguNTU3IDEuNjIzLjk0NC44NTUuMzg3IDEuNzgxLjU4NlExMi41NCAyMSAxMy41IDIxek01LjgxMiA5LjU5OHEuNTc1IDAgLjkxNS4yMjguMzQuMjI5LjM0LjgzOCAwIC4yNy0uMTI0LjQ0LS4xMjMuMTctLjMxLjI3NS0uMTg4LjEwNS0uNDIyLjE0Ni0uMjM0LjA0MS0uNDQ1LjA0MUg0LjY4N1Y5LjU5OFoiIC8%2BPC9zdmc%2B`
   - C、C++、Arduino、ESP32、Raspberry Pi 沿用当前示例配色与图标：
     - C：`https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black`
     - C++：`https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white`
     - Arduino：`https://img.shields.io/badge/Arduino-00878F?style=flat-square&logo=arduino&logoColor=white`
     - ESP32：`https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white`
     - Raspberry Pi：`https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white`
   - Python 徽章统一使用 RGB(47, 76, 108)，即 #2F4C6C 作为整个徽章的背景色，文字 Python 为白色，左侧使用 Python 官方黄蓝双色双蛇 SVG 图标。保持原图形、双色渐变与比例、flat-square 样式及 20px 高度。直接复用配套的静态 SVG，不把完整 Python SVG 塞进 Shields.io URL，以免 GitHub 图片代理返回 `URI Too Long`。将文件与 README 一起交付，并按文档位置调整路径：
     `![Python](./assets/python-badge.svg)`
     资源地址：`https://raw.githubusercontent.com/CCU-Robotics-Association/CRA-Skill-Prompt/main/prompts/readme/assets/python-badge.svg`
   - Java 徽章保留橙色 #ED8B00 背景与白色 Java 文字，左侧添加白色咖啡杯 SVG Logo，保持图标比例、flat-square 样式及 20px 高度。使用以下链接：
     `https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMjggMTI4IiB3aWR0aD0iMTI4IiBoZWlnaHQ9IjEyOCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTQ3LjYxNyA5OC4xMmMtMTkuMTkyIDUuMzYyIDExLjY3NyAxNi40MzkgMzYuMTE1IDUuOTY5LTQuMDAzLTEuNTU2LTYuODc0LTMuMzUxLTYuODc0LTMuMzUxLTEwLjg5NyAyLjA2LTE1Ljk1MiAyLjIyMi0yNS44NDQgMS4wOTItOC4xNjQtLjkzNS0zLjM5Ny0zLjcxLTMuMzk3LTMuNzF6bTMzLjE4OS0xMC40NmMtMTQuNDQ0IDIuNzc5LTIyLjc4NyAyLjY5LTMzLjM1NCAxLjYtOC4xNzEtLjg0NS0yLjgyMi00LjgwNS0yLjgyMi00LjgwNS0yMS4xMzcgNy4wMTYgMTEuNzY3IDE0Ljk3NyA0MS4zMDkgNi4zMzYtMy4xNC0xLjEwNi01LjEzMy0zLjEzMS01LjEzMy0zLjEzMXptMTEuMzE5LTYwLjU3NWMuMDAxIDAtNDIuNzMxIDEwLjY2OS0yMi4zMjMgMzQuMTg3IDYuMDI0IDYuOTM1LTEuNTggMTMuMTctMS41OCAxMy4xN3MxNS4yODktNy44OTEgOC4yNjktMTcuNzc3Yy02LjU1OS05LjIxNS0xMS41ODctMTMuNzkzIDE1LjYzNC0yOS41OHptOS45OTggODEuMTQ0czMuNTI5IDIuOTEtMy44ODggNS4xNTljLTE0LjEwMiA0LjI3Mi01OC43MDYgNS41Ni03MS4wOTUuMTcxLTQuNDUtMS45MzggMy44OTktNC42MjUgNi41MjYtNS4xOTIgMi43MzktLjU5MyA0LjMwMy0uNDg1IDQuMzAzLS40ODUtNC45NTItMy40ODctMzIuMDEzIDYuODUtMTMuNzQyIDkuODE1IDQ5LjgyMSA4LjA3NiA5MC44MTctMy42MzcgNzcuODk2LTkuNDY4ek04NSA3Ny44OTZjMi4zOTUtMS42MzQgNS43MDMtMy4wNTMgNS43MDMtMy4wNTNzLTkuNDI0IDEuNjg1LTE4LjgxMyAyLjQ3NGMtMTEuNDk0Ljk2NC0yMy44MjMgMS4xNTQtMzAuMDEyLjMyNi0xNC42NTItMS45NTkgOC4wMzMtNy4zNDggOC4wMzMtNy4zNDhzLTguODEyLS41OTYtMTkuNjQ0IDQuNjQ0QzE3LjQ1NSA4MS4xMzQgNjEuOTU4IDgzLjk1OCA4NSA3Ny44OTZ6bTUuNjA5IDE1LjE0NWMtLjEwOC4yOS0uNDY4LjYxNi0uNDY4LjYxNiAzMS4yNzMtOC4yMjEgMTkuNzc1LTI4Ljk3OSA0LjgyMi0yMy43MjUtMS4zMTIuNDY0LTIgMS41NDMtMiAxLjU0M3MuODI5LS4zMzQgMi42NzgtLjcyYzcuNTU5LTEuNTc1IDE4LjM4OSAxMC4xMTktNS4wMzIgMjIuMjg2ek02NC4xODEgNzAuMDY5Yy00LjYxNC0xMC40MjktMjAuMjYtMTkuNTUzLjAwNy0zNS41NTlDODkuNDU5IDE0LjU2MyA3Ni40OTIgMS41ODcgNzYuNDkyIDEuNTg3YzUuMjMgMjAuNjA4LTE4LjQ1MSAyNi44MzMtMjYuOTk5IDM5LjY2Ny01LjgyMSA4Ljc0NSAyLjg1NyAxOC4xNDIgMTQuNjg4IDI4LjgxNXptMjcuMjc0IDUxLjc0OGMtMTkuMTg3IDMuNjEyLTQyLjg1NCAzLjE5MS01Ni44ODcuODc0IDAgMCAyLjg3NCAyLjM4IDE3LjY0NiAzLjMzMSAyMi40NzYgMS40MzcgNTctLjggNTcuODE2LTExLjQzNi4wMDEgMC0xLjU3IDQuMDMyLTE4LjU3NSA3LjIzMXoiIC8%2BPC9zdmc%2B`
   - MATLAB 徽章统一使用白色 #FFFFFF 背景、蓝色 #0076A8 的 MATLAB 文字，左侧添加 MATLAB 原有彩色 SVG Logo。保持方形、无阴影的 flat-square 外观及 20px 高度，字体为 11px Verdana/Geneva/DejaVu Sans/sans-serif。制作或复用静态 SVG，准确设置文字颜色，将 SVG 文件与 README 一起交付。默认保存为 assets/matlab-badge.svg，按 README 所在目录调整引用路径：
     `![MATLAB](./assets/matlab-badge.svg)`
     彩色 Logo 来源：https://raw.githubusercontent.com/devicons/devicon/master/icons/matlab/matlab-original.svg。保留原有渐变和图形比例，并将图形嵌入徽章 SVG，确保徽章可独立显示。
   - Markdown 徽章统一使用白色 #FFFFFF 背景、黑色文字，左侧保留 Markdown Logo 并设为黑色 #000000，保持 flat-square 样式及 20px 高度。使用以下链接：
     `https://img.shields.io/badge/Markdown-ffffff?style=flat-square&logo=markdown&logoColor=000000`
   - OpenCV 徽章统一使用白色 #FFFFFF 背景、黑色 OpenCV 文字，左侧使用红、绿、蓝三色环形 SVG 图标，保留原始彩色和比例，通过 Base64 SVG 嵌入 logo 参数，保持 flat-square 样式及 20px 高度。使用以下链接：
     `https://img.shields.io/badge/OpenCV-ffffff?style=flat-square&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMjggMTI4IiB3aWR0aD0iMTI4IiBoZWlnaHQ9IjEyOCI%2BPHBhdGggZD0iTTExMi44NzEgNjYuNjAyYzkuMDA0IDUuMjc3IDE1LjA1NSAxNS4wMjcgMTUuMDc0IDI2LjE5MS4wMzIgMTYuODA1LTEzLjYxNyAzMC40NTMtMzAuNDggMzAuNDgtMTYuODYzLjAzMi0zMC41NTktMTMuNTctMzAuNTktMzAuMzc1LS4wMi0xMS4xNjQgNS45OTYtMjAuOTMzIDE0Ljk4NC0yNi4yNDZsOC43NzQgMTQuNzc4Yy4yMTkuMzcuMDk0Ljg0Ny0uMjYyIDEuMDktMy4zMiAyLjI1LTUuNDk2IDYuMDQ2LTUuNDg4IDEwLjM0Ny4wMTIgNi44OTUgNS42MzMgMTIuNDc3IDEyLjU1IDEyLjQ2MSA2LjkxOS0uMDEyIDEyLjUxNi01LjYxIDEyLjUwNC0xMi41MDQtLjAwNy00LjMtMi4xOTUtOC4wOS01LjUyMy0xMC4zMjgtLjM1NS0uMjQyLS40ODQtLjcxOS0uMjY2LTEuMDl6bTAgMCIgZmlsbD0iIzEyOGRmZiIgLz48cGF0aCBkPSJNNDUuNDc3IDY2LjQyMmEzMC40OTUgMzAuNDk1IDAgMDAtMTQuOTA3LTMuODY3QzEzLjcwMyA2Mi41NTUuMDM1IDc2LjE4LjAzNSA5Mi45ODVjMCAxNi44MDQgMTMuNjY4IDMwLjQzIDMwLjUzNSAzMC40MyAxNi45NDYgMCAzMC45NS0xNC4zMzcgMzAuNTI0LTMxLjIxMkg0My45MDZjLS40NTMgMC0uODA4LjM4My0uODEyLjgzMi0uMDQzIDYuNzIzLTUuNjcyIDEyLjQzNC0xMi41MjQgMTIuNDM0LTYuOTIyIDAtMTIuNTI3LTUuNTktMTIuNTI3LTEyLjQ4NSAwLTYuODk0IDUuNjA1LTEyLjQ4NCAxMi41MjctMTIuNDg0IDEuODA5IDAgMy41MzIuMzgzIDUuMDg2IDEuMDc0LjM4My4xNjguODM2LjA0IDEuMDQ3LS4zMTZ6bTAgMCIgZmlsbD0iIzhiZGE2NyIgLz48cGF0aCBkPSJNNDcuOTQ1IDYxLjY0OGMtOC45OTItNS4yOTMtMTUuMDI3LTE1LjA1NC0xNS4wMjctMjYuMjE4QzMyLjkxOCAxOC42MjUgNDYuNTkgNSA2My40NTMgNXMzMC41MzUgMTMuNjI1IDMwLjUzNSAzMC40M2MwIDExLjE2NC02LjAzNSAyMC45MjUtMTUuMDI3IDI2LjIxOEw3MC4yMSA0Ni44NmMtLjIxOS0uMzctLjA5NC0uODQ3LjI2Ni0xLjA5IDMuMzItMi4yNDYgNS41MDMtNi4wMzkgNS41MDMtMTAuMzQgMC02Ljg5NC01LjYwOS0xMi40ODQtMTIuNTI3LTEyLjQ4NC02LjkxOCAwLTEyLjUyNyA1LjU5LTEyLjUyNyAxMi40ODUgMCA0LjMgMi4xODMgOC4wOTMgNS41MDQgMTAuMzQuMzYuMjQyLjQ4NC43MTguMjY1IDEuMDl6bTAgMCIgZmlsbD0iI2ZmMmE0NCIgLz48L3N2Zz4%3D`
   - PyTorch 徽章统一使用白色 #FFFFFF 背景、黑色 PyTorch 文字，左侧保留 PyTorch Logo，使用橙红色 #EE4C2C，保持 flat-square 样式及 20px 高度。使用以下链接：
     `https://img.shields.io/badge/PyTorch-ffffff?style=flat-square&logo=pytorch&logoColor=EE4C2C`
   - TensorFlow 徽章统一使用白色 #FFFFFF 背景、黑色 TensorFlow 文字，左侧保留 TensorFlow Logo，使用橙色 #FF6F00，保持 flat-square 样式及 20px 高度。使用以下链接：
     `https://img.shields.io/badge/TensorFlow-ffffff?style=flat-square&logo=tensorflow&logoColor=FF6F00`
   - Keras 徽章统一使用白色 #FFFFFF 背景、黑色 Keras 文字，左侧保留 Keras Logo，使用红色 #D00000，保持 flat-square 样式及 20px 高度。使用以下链接：
     `https://img.shields.io/badge/Keras-ffffff?style=flat-square&logo=keras&logoColor=D00000`
   - NumPy 徽章统一使用白色 #FFFFFF 背景、黑色 NumPy 文字，左侧保留 NumPy Logo，使用深蓝绿色 #013243，保持 flat-square 样式及 20px 高度。使用以下链接：
     `https://img.shields.io/badge/NumPy-ffffff?style=flat-square&logo=numpy&logoColor=013243`
   - pandas 徽章统一使用白色 #FFFFFF 背景、黑色 Pandas 文字，左侧保留 pandas Logo，使用深紫色 #150458，保持 flat-square 样式及 20px 高度。使用以下链接：
     `https://img.shields.io/badge/Pandas-ffffff?style=flat-square&logo=pandas&logoColor=150458`
   - YOLO 徽章统一使用白色 #FFFFFF 背景、黑色 YOLO 文字，左侧使用蓝色至青色渐变的彩色 YOLO Logo，保留渐变填充与原始比例，通过 Base64 SVG 嵌入 logo 参数。保持 flat-square 样式及 20px 高度，文字仅显示 YOLO，不附加 Object Detection。使用以下链接：
     `https://img.shields.io/badge/YOLO-ffffff?style=flat-square&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB3aWR0aD0iMTE0IiBoZWlnaHQ9IjEyMCIgdmlld0JveD0iMCAwIDExNCAxMjAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI%2BPGcgY2xpcC1wYXRoPSJ1cmwoI2NsaXAwXzEyNzM3XzQ5Mzg4KSI%2BPG1hc2sgaWQ9Im1hc2swXzEyNzM3XzQ5Mzg4IiBzdHlsZT0ibWFzay10eXBlOmx1bWluYW5jZSIgbWFza1VuaXRzPSJ1c2VyU3BhY2VPblVzZSIgeD0iLTEiIHk9IjIiIHdpZHRoPSIxMTYiIGhlaWdodD0iMTE4Ij48cGF0aCBkPSJNMTE0LjE3OSAyLjc1NzgxSC0wLjE5NTMxMlYxMTkuOTY5SDExNC4xNzlWMi43NTc4MVoiIGZpbGw9IndoaXRlIiAvPjwvbWFzaz48ZyBtYXNrPSJ1cmwoI21hc2swXzEyNzM3XzQ5Mzg4KSI%2BPHBhdGggZD0iTTI2LjU4IDIuNzU3ODFDMTEuODE1OSAyLjc1NzgxIC0wLjE5NTMxMiAxNC44MzIxIC0wLjE5NTMxMiAyOS42NzM0Qy0wLjE5NTMxMiA0NC41MTM3IDExLjgxNTkgNTYuNTg4MyAyNi41OCA1Ni41ODgzQzQxLjM0NDMgNTYuNTg4MyA1My4zNTU1IDQ0LjUxMzcgNTMuMzU1NSAyOS42NzM0QzUzLjM1NTUgMTQuODMyMSA0MS4zNDQzIDIuNzU3ODEgMjYuNTggMi43NTc4MVoiIGZpbGw9IiMwQjIzQTkiIC8%2BPHBhdGggZD0iTTU2Ljg3NTEgODcuMDQxOUM0Ny4yMzAzIDg3LjA0MTkgMzguMTE3IDg0LjU4NzEgMzAuMTE3MiA4MC4yNzcxVjkyLjQ4ODNDMzAuMTE3MiAxMDcuMzA3IDQxLjg4OCAxMTkuNjAyIDU2LjYyODYgMTE5Ljc0NUM3MS41MTM3IDExOS44OSA4My42Njg3IDEwNy43NiA4My42Njg3IDkyLjgzMTVWODAuMjY1NkM3NS42NjEzIDg0LjU4NjQgNjYuNTMzMiA4Ny4wNDE5IDU2Ljg3NTEgODcuMDQxOVoiIGZpbGw9IiMwQjIzQTkiIC8%2BPHBhdGggZD0iTTYwLjM4IDI5LjY3OTZDNjAuMzUyMiA0OC40MDMyIDQ1LjIzMTMgNjMuNjA5IDI2LjUzODMgNjMuNjU0OEMxOS4zMjc0IDYzLjY3MzYgMTIuNTYwOSA2MS40MTcgNy4wMzkwNiA1Ny40Nzc2QzE2LjgyNTkgNzUuMDYzNyAzNS41MDA4IDg3LjA1NDQgNTYuODU0NSA4Ny4wMTI4Qzg3Ljg3NDEgODcuMDM3NSAxMTMuNDcgNjEuNjUwNSAxMTMuOTg3IDMwLjUxNEwxMTMuOTE0IDMwLjQ0NzRDMTEzLjk0NCAyOS42NzE2IDExMy45MDYgMzAuMzA3MSAxMTMuOTQ0IDI5LjY3MTZDMTEzLjk1OSAxNC44MTk4IDEwMS45MjkgMi42OTg0NiA4Ny4yMjgyIDIuNzUwMTZDNzIuMzg3MSAyLjgwOTA1IDYwLjM5NDggMTQuODI3NiA2MC4zOCAyOS42Nzk2WiIgZmlsbD0idXJsKCNwYWludDBfbGluZWFyXzEyNzM3XzQ5Mzg4KSIgLz48L2c%2BPC9nPjxkZWZzPjxsaW5lYXJHcmFkaWVudCBpZD0icGFpbnQwX2xpbmVhcl8xMjczN180OTM4OCIgeDE9IjMyLjE5MTciIHkxPSI4Ni4wNjA3IiB4Mj0iOTguODM4MSIgeTI9IjEyLjYxNTciIGdyYWRpZW50VW5pdHM9InVzZXJTcGFjZU9uVXNlIj48c3RvcCBzdG9wLWNvbG9yPSIjMDlEQkYwIiAvPjxzdG9wIG9mZnNldD0iMSIgc3RvcC1jb2xvcj0iIzBCMjNBOSIgLz48L2xpbmVhckdyYWRpZW50PjxjbGlwUGF0aCBpZD0iY2xpcDBfMTI3MzdfNDkzODgiPjxyZWN0IHdpZHRoPSIxMTQiIGhlaWdodD0iMTIwIiBmaWxsPSJ3aGl0ZSIgLz48L2NsaXBQYXRoPjwvZGVmcz48L3N2Zz4%3D`
   - STM32 徽章统一使用黄色 #FFD200 背景、黑色 STM32 文字，左侧使用深蓝色 #03234B 的 STMicroelectronics 标志，保持 flat-square 样式及 20px 高度。使用以下链接：
     `https://img.shields.io/badge/STM32-FFD200?style=flat-square&logo=stmicroelectronics&logoColor=03234B`
   - ROS 徽章统一使用白色 #FFFFFF 背景、黑色 ROS 文字，左侧保留深蓝色 #22314E 的 ROS 九点 Logo，保持 flat-square 样式及 20px 高度。使用以下链接：
     `https://img.shields.io/badge/ROS-ffffff?style=flat-square&logo=ros&logoColor=22314E`
   - 年份徽章与文字时间范围保持一致。例如 `2024——Future` 对应 `2024%E2%80%94%E2%80%94Future`。
   - 只有仓库已明确声明许可证时才添加 License 徽章，不因参考示例中有 MIT 就直接沿用。
   - 所有开源许可证徽章统一参考 MIT 示例的配色与布局：左侧白底黑字显示实际许可证名称，右侧黑底白字固定显示 License，保持 flat-square 样式。适用于 MIT、Apache-2.0、GPL-3.0、BSD-3-Clause 等开源许可证，仅替换左侧名称，配色保持一致。许可证名称与版本必须以仓库实际声明为准。
   - 通用链接格式为 `https://img.shields.io/badge/{经过 Shields.io 路径编码的许可证名称}-License-000000?style=flat-square&labelColor=ffffff`。名称中的连字符需写成双连字符 `--`，例如 `Apache--2.0`。MIT 示例：
     `https://img.shields.io/badge/MIT-License-000000?style=flat-square&labelColor=ffffff`
   - 开源项目可添加以下 Open Source 徽章：左侧黑底白字 Open，右侧白底黑字 Source，保持 flat-square 样式：
     `https://img.shields.io/badge/Open-Source-ffffff?style=flat-square&labelColor=000000`

8. 添加加粗的导航链接，使用 ` | ` 分隔。固定包含以下入口，其余入口根据当前主题选择：
   - `官网(Website) »`：`https://ccu-robotics-association.github.io/`
   - `GitHub 主页 »`：`https://github.com/CCU-Robotics-Association`
   - 其他入口按主题选择，页首标签使用中文或中英结合的名称，并以 ` »` 结尾，例如 `视觉媒体资源(VMA) »`、`提交指南(Commit) »`。
   - 需要提交指南时，使用当前目录下有效的相对路径，或已核实的完整地址。协会公共指南的现有地址为 `https://github.com/CCU-Robotics-Association/.github/blob/main/profile/CONTRIBUTING.md`。
   - 保留原文已经选择的入口名称、目标链接及相对路径，不把有效的导航统一改成另一套措辞。

9. 使用引用块展示固定标语，保持加粗和字间空格：

   ```markdown
   > **一  同  奋  进  前  行  ，  共  就  非  凡  之  事**
   ```

10. 关闭页首的 `</div>`，空行后使用 `---` 分隔正文。

## 正文规则

- 章节标题采用“SVG 图标 + English | 中文”的格式，使用竖线分隔双语标题。图标通过 `<img>` 引入，例如：

  ```markdown
  ## <img src="./assets/icons/users-round.svg" width="22" height="22" alt=""> Author | 历届作者
  ```

- 正文采用简短直接的中文，保留示例中的精炼措辞，例如“查看提交要求”“依年份整理保留”。除长篇大段文字外，不加句尾句号；标题、表格单元格、列表条目、简短说明和提示块中的短句均遵循此规则。长段落按需要使用正常标点，保留正文中的逗号、冒号及必要的问号、感叹号等。
- 文本强调按用途使用：正文关键术语可沿用 `***CRA***`、`***GitHub***` 的加粗斜体，条目名称和关键词使用 `**加粗**`，文件命名规范使用行内代码。
- 使用统一的线性 SVG 图标，默认不用 Emoji。徽章的品牌 Logo 与正文章节图标分别沿用各自的样式。
- 根据当前主题组织章节，保持适当留白。短列表用于并列操作，表格用于年度、作者或内容分类，双栏 HTML 表格用于两个并列入口或维护要求。
- 检查事项使用普通无序列表，直接写需要检查的内容。禁止使用 Markdown 任务列表语法（`- [ ]`、`- [x]`）、HTML 复选框或方框符号；即使标题为 Checklist 或“最终检查”，也不添加勾选框。例如写成 `- 检查图片路径与链接是否有效`。
- 编辑现有资料页时保留它的内容范围，不自动补回用户已删去的文件清单、文件大小、下载步骤或 Git LFS 教程。
- 文档作者记录在顶部隐藏注释中。公开的历届作者表记录资料本身的作者，两者分开处理。
- 作者按上述输入规则确定，年份、技术栈、文件大小、许可证和链接都必须有资料依据。信息缺失时使用明确占位文字，不编造；缺少有效 URL 的入口不生成伪链接。
- 保留原有文件名、真实年份及有效链接。修改文件名时同步更新对应链接，注意空格和中文路径。
- 维护说明只写与当前资料有关的要求，如文件命名、内容完整性或实际使用的存储方式。
- 使用 GitHub 支持的 Markdown 与简单 HTML。块级 HTML 和 Markdown 之间保留空行，确保预览能够正确渲染。
- 可以根据内容适量使用 GitHub 原生提示块，突出补充说明、操作建议、重要要求或风险提醒，避免每段都加。类型按用途选择：`NOTE` 用于补充信息，`TIP` 用于实用建议，`IMPORTANT` 用于关键要求，`WARNING` 用于需要留意的风险，`CAUTION` 用于可能造成数据丢失等严重后果的操作。警告类型使用 `WARNING`，不要写成 `WARN`。提示块前后保留空行，正文每行以 `>` 开头，例如：

  ```markdown
  > [!NOTE]
  > 此处填写与当前内容有关的补充说明

  > [!WARNING]
  > 此处填写需要留意的操作风险
  ```

## SVG 图标规范

- 优先复用现有 `assets/icons/` 中的 Lucide SVG 图标，保持原始线条、比例和图形结构，描边统一为紫色 `#8B5CF6`。
- 新增图标时，可从 `https://raw.githubusercontent.com/lucide-icons/lucide/main/icons/{图标名}.svg` 获取对应 SVG，保留其许可声明。仓库中的 `assets/icons/LICENSE` 应随图标保留。
- 图标用 `<img src="...svg">` 引入，采用支持的 `width`、`height` 属性控制大小。装饰性图标使用 `alt=""`，旁边保留完整的文字说明。
- 不依赖前端组件、图标字体、JavaScript 或自定义 CSS 来显示图标。
- 尺寸按场景统一：章节标题 22×22px，双栏模块顶部 28×28px，表格与列表内 18×18px。页首协会 Logo 单独保持 132px 宽度。

## 双栏布局写法

两个并列入口或维护事项采用以下结构。替换图标、标题、内容和链接，保留块级 HTML 与 Markdown 之间的空行：

```markdown
<table>
<tr>
<td width="50%" valign="top">

<img src="./assets/icons/presentation.svg" width="28" height="28" alt="">

### Naming | 命名规范

`实际文件命名格式`

简短说明

</td>
<td width="50%" valign="top">

<img src="./assets/icons/circle-check.svg" width="28" height="28" alt="">

### Check | 文件检查

**需要检查的内容**

简短说明

</td>
</tr>
</table>
```

## 统一页脚

正文结束后先添加 `---`，再按以下结构编排页脚。将占位内容替换为当前文档对应的信息。导航文字全部加粗，各入口使用 ` · ` 分隔，页脚链接不添加页首的 ` »` 后缀：

```markdown
<div align="center">

### CCU · ROBOTICS · ASSOCIATION

<sub>中文资料主题 | 仓库名称或简称</sub>

[**官网(Website)**](https://ccu-robotics-association.github.io/) · [**GitHub 主页**](https://github.com/CCU-Robotics-Association) · [**中文入口(English)**](有效地址)

<sub>CCU Robotics Association</sub>

</div>
```

- 资料归档示例的副行使用 `历届招新 PPT | CRA Visual Media Assets`，第三个入口使用 `招新 PPT(Recruitment)`。
- 社区主页示例的副行使用 `CRA GitHub 社区 | CRA .github`，第三个入口使用 `提交指南(Contributing)`。
- 其他主题使用对应的资料名称、仓库名称和有效入口，保留相同的结构与大小写风格。

## 图片资源与检查

- 本地图标和自定义徽章使用相对于 README 的路径。README 位于不同目录时，调整引用路径或将所需资源一同放入对应目录。
- 使用 `assets/icons/` 或 `assets/matlab-badge.svg` 等本地资源时，交付对应 SVG 文件及必要许可文件，确保其他人获取文档后也能显示图片。
- 本 Prompt 的配套资源位于 [README Prompt 配套资源](https://github.com/CCU-Robotics-Association/CRA-Skill-Prompt/tree/main/prompts/readme/assets)。图标、Python 与 MATLAB 徽章可以直接复用；从这个仓库复制到目标仓库后再使用本地路径，不要求目标仓库原先就有这些文件。仅需某几个图标时，只复制实际使用的 SVG 及对应许可说明。
- 对可正常使用的短 URL，完整保留嵌入的 Base64 SVG；复杂 Logo 导致链接过长、无法通过 GitHub 图片代理时，改为随仓库提交的静态 SVG 徽章，并同步更新引用。不要只在本地预览通过就视为 GitHub 可用。彩色和渐变 Logo 保持当前图形、色彩和比例，不替换成单色版本。
- 修改完成后检查图片路径、链接、HTML 表格和 Markdown 渲染；检查顶部徽章是否仍在原位置、原顺序，保留已有空行分组。

## 交付前核对

- 作者注释位于第一行，Logo 保持透明 SVG 与 132px 宽度，一级标题为固定协会名称。
- 年份来自资料；顶部包含协会专属徽章且不含 `AREA ROBOTICS`；其余徽章仅保留与当前主题有关且已选定的内容。
- 导航目标有效；双语标题、双栏布局、提示块和折叠命令在 GitHub Markdown 中可正常阅读；不为使用格式而硬加无关章节。
- 图片、徽章、锚点与相对链接均已核对，随文档交付实际使用的本地资源及许可说明。
- 文件保留原有有效信息，未加入真实密钥、虚构事实或生成过程。只有明确标识为待补全的信息才允许保留占位文字。

## 输出要求

输出最终 README 的完整 Markdown 源码，保留顶部 HTML 作者注释；如使用本地 SVG，同时提供必要资源。不要在文档正文中加入生成过程、检查记录或无关解释。默认仅修改我指定的文档及所需的图片资源；除非我明确要求，否则不上传、不提交、不发布，也不修改其他参考文档。
