# VS Code Settings & Snippets

个人 VS Code 配置文件备份，包含自定义代码片段和编辑器设置。

## 📁 项目结构

```
vscode_settings_json/
├── FileHeader.code-snippets    # 文件头注释代码片段
├── .vscode/
│   └── settings.json           # 工作区配置（颜色主题自定义）
└── README.md
```

## 🚀 安装使用

### 代码片段安装路径

将 `FileHeader.code-snippets` 复制到以下路径：

| 操作系统    | 路径                                                |
| ----------- | --------------------------------------------------- |
| **Windows** | `%APPDATA%\Code\User\snippets\`                     |
| **macOS**   | `~/Library/Application Support/Code/User/snippets/` |
| **Linux**   | `~/.config/Code/User/snippets/`                     |

#### 完整路径示例

- **Windows**: `C:\Users\<用户名>\AppData\Roaming\Code\User\snippets\`
- **macOS**: `/Users/<用户名>/Library/Application Support/Code/User/snippets/`
- **Linux**: `/home/<用户名>/.config/Code/User/snippets/`

> 💡 **提示**: 如果使用 VS Code Insiders 版本，将路径中的 `Code` 替换为 `Code - Insiders`

## 📝 代码片段说明

### FileHeader.code-snippets

文件头注释模板，输入 `sni` 触发，支持多种编程语言：

| 触发前缀 | 支持的语言                                         | 注释风格        |
| -------- | -------------------------------------------------- | --------------- |
| `sni`    | C#, JavaScript, TypeScript, Java, C++, C, Go, Rust | `/* */` 块注释  |
| `sni`    | Python, Shell, YAML, Dockerfile                    | `#` 行注释      |
| `sni`    | HTML, XML                                          | `<!-- -->` 注释 |

#### 示例输出（C-style）

```javascript
/**
 * File: example.js
 * Author: eneisyou
 * Email: eneisyou@gmail.com
 * Created: 2025-12-25
 * Description: 示例文件描述
 */
```

#### 示例输出（Python）

```python
#!/usr/bin/env python3
# -*- coding: utf-8 -*-

# File: example.py
# Author: eneisyou
# Email: eneisyou@gmail.com
# Created: 2025-12-25
# Description: 示例文件描述
```

## 🎨 编辑器主题配置

`.vscode/settings.json` 包含自定义的编辑器颜色配置：

- **查找匹配高亮**: 橙色/黄绿色
- **选中文本**: 蓝色半透明
- **Diff 编辑器**: 自定义插入/删除背景色
- **活动标签页**: 青色高亮
- **活动栏/标题栏**: 深绿色主题

## 📋 快速安装命令

### Windows (PowerShell)

```powershell
# 复制代码片段
Copy-Item "FileHeader.code-snippets" "$env:APPDATA\Code\User\snippets\"
```

### macOS / Linux

```bash
# macOS
cp FileHeader.code-snippets ~/Library/Application\ Support/Code/User/snippets/

# Linux
cp FileHeader.code-snippets ~/.config/Code/User/snippets/
```

## 📄 License

MIT License

---

⭐ 如果这个配置对你有帮助，欢迎 Star！

# Texの日本語フォーマット配置
## 【LaTeX】Vs code下载与配置

TeX Live 下载与安装

链接：https://pan.quark.cn/s/936429147d2c?pwd=P8dX
提取码：P8dX

方法一：下载安装包
访问 TeX Live 官网。各平台对应的安装程序如下：

Windows: install-tl-windows.exe (网络安装器)
Linux: install-tl-unx.tar.gz (解压后运行 install-tl 脚本)
macOS: MacTeX-年份.pkg (完整的 MacTeX 发行版)

方法二：下载iso镜像
官方下载页（ISO）：https://tug.org/texlive/acquire-iso.html → 点击downloadfromanearbyCTANmirror → 下载 texlive.iso。

---
镜像源
下列是一些国内镜像源，点开后点击 systems → TeX Live 进行下载，Source/ 对应方法一，Images/ 对应方法二：

国内 CTAN 镜像站点列表：

阿里云 (Aliyun)
北京外国语大学 (BFSU)
清华大学 (TUNA)
中国科学技术大学 (USTC)
上海交通大学 (SJTUG)
南京大学 (NJU)
北京大学 (PKU)
腾讯云 (Tencent Cloud)
哈尔滨工业大学 (HIT)
重庆大学 (CQU)
吉林大学 (JLU)
南方科技大学 (SUSTech)
浙江大学 (ZJU)

---
启动安装器：

ISO/镜像: 下载完成后，双击 ISO 或右键装载为虚拟光驱。在根目录找到 install-tl-windows.bat。

网络安装包: 直接运行下载的 install-tl-windows.exe。
重要：请右键点击安装程序，选择“以管理员身份运行”，以确保其有权限修改系统 PATH 环境变量。

---
配置安装选项：

进入主安装界面后，你需要关注几个基本更改：

安装路径：默认路径为 C:\texlive\2025。如果 C 盘空间紧张，可以修改到其他盘符，例如 D:\texlive\2025。路径中避免使用中文或空格。

前端组件：默认会安装 TeXworks 编辑器。如果你计划使用 VS Code，可以在组件页中取消勾选 TeXworks front end。
PATH：新版本的 Windows 安装器默认会将 TeX Live 的 bin 目录添加到系统 PATH。

如果你想节省磁盘空间，可以点击“选择 (Selections)”下的“定制 (Customize)”，在“语言 (Languages)”标签页中，只保留“中文 (Chinese)”和“英美英文 (US and UK English)”这两个语言集合。

---
开始安装：

点击 安装(Install) 按钮开始安装。这个过程会从镜像源下载大量宏包，根据你的网络速度和磁盘性能，耗时可能较长（30分钟到数小时不等）。

(3) 验证是否安装成功
Windows（PowerShell）
# 1) 验证 XeLaTeX 引擎版本
xelatex -v

# 2) 验证 TeX Live 管理器版本
tlmgr --version

# 3) 确认 PATH 指向当前年份的 bin 目录
where xelatex
image.png
image.png

更换/修复 PATH（如未写入或曾取消）
TeX Live 官方提供 tlmgr path 子命令用于添加/移除系统可执行路径映射（Windows 会创建合适的“前端链接”）。示例：
tlmgr path add
# 如需撤销：
tlmgr path remove
该子命令行为以《tlmgr 手册》为准。

回滚包版本（出现包更新问题时）
tlmgr 默认保留一次备份。可用：
- 回滚所有包到最近备份
tlmgr restore --all
- 或针对单包：
tlmgr restore <pkg> <revision>
macOS / Linux（bash）
- 1) 引擎版本
xelatex -v

- 2) 管理器版本
tlmgr --version

- 3) 确认 PATH（找不到命令时）
which xelatex
- 如 PATH 有误，可用：
tlmgr path add



### 安装 VS Code 与 LaTeX Workshop

安装 TeX Live 只是提供了底层的编译引擎和宏包，我们还需要一个现代化的编辑器来编写 .tex 文稿。VS Code 配合 LaTeX Workshop 扩展是目前最高效的组合之一。

下载 VS Code：

官方下载：https://code.visualstudio.com/Download
博客教程：【VS Code】告别安装与配置困难
安装 LaTeX Workshop 扩展：

打开 VS Code，在左侧菜单栏中打开“扩展”视图，搜索并安装 LaTeX Workshop。

提示：安装完成后，只有当你打开或新建一个 .tex 文件时，左侧菜单栏才会出现 TEX 图标（LaTeX Workshop 的专属面板）。
image.png
image.png

关键配置 (settings.json)
为了获得最佳体验（尤其是中文支持和整洁的项目目录），我们需要对 LaTeX Workshop 进行配置。

追加 settings.json 中的内容：

- 快速自测

Hello, XeLaTeX（新建 main.tex）：

\documentclass{ctexart} % 中文友好
\begin{document}
你好，\LaTeX！这是 XeLaTeX 自测。我是泪花花。
\end{document}
