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
