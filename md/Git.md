---
title: Git Manual
tags: []
notebook: Man
---

# Git Manual

[TOC]

## Overview
Git is a version control system for tracking changes in files, primarily used for source code management in software development.

## Install & Config
### Windows
1. Download and install [git-for-windows](http://msysgit.github.io/)
2. <kbd>ctrl</kbd> <kbd>`</kbd> to open console
3. Paste [code from packagecontrol.io](https://packagecontrol.io/installation)
4. <kbd>ctrl</kbd> <kbd>shift</kbd> <kbd>p</kbd> to open command palatte
5. `install` other plug-ins by name

### Useful plug-ins
+ **ConvertToUTF8** -- 支持 GBK, BIG5, EUC-KR, EUC-JP, Shift_JIS 等编码
+ **Bracket Highlighter** -- 用于匹配括号，引号和html标签
+ **SideBar Enhancements** -- 加强了侧边栏，增加了许多功能
+ **Themr** -- 主题管理和切换
+ **Emmet(Zen Coding)** -- 快速生成HTML代码段的强大插件

### Sublime w/ Markdown

#### SublimeTmpl 与 md 模板
1. 安装 **SublimeTmpl** 插件
2. 通过 `Preferences` -> `Browse Packages...` 到达 Packages 文件夹
3. 进入 `...\Packages\SublimeTmpl\templates` 新建 md.tmpl 并加入以下内容并保存
>
\-\-\-
title: New title
tags: []
notebook: Notes
\-\-\-
4. 进入 `File` -> `New file (SublimeTmpl)` -> `Menu - Default` 并在对应位置加入
>
{
    "id": "md",
    "caption": "md",
    "command": "sublime_tmpl",
    "args": {
        "type": "md"
    }
},
5. 进入 `Preferences` -> `Key Bindings` 中，在 User 配置文件中加入
>
{
    "keys": ["ctrl+alt+m"], "command": "sublime_tmpl", "args": {"type":"md"},"context":[{"key":"sublime_tmpl.md"}]
}
6. 之后就可以通过 <kbd>ctrl</kbd> <kbd>alt</kbd> <kbd>m</kbd> 新建 md 模板的文件

#### Markdown Preview
1. 安装 **Markdown Preview** 插件
2. 进入 `Preferences` -> `Package Settings` -> `Markdown Preview` > `Settings - User` 并加入
>
{
    "build_action": "browser",
    "enable_mathjax": true,
    "enable_uml": true
}
3. 之后就可以通过 <kbd>ctrl</kbd> <kbd>b</kbd> 在浏览器预览效果

#### Markdown Editing
1. 安装 **Markdown Editing** 插件
2. 进入 `Preferences` -> `Package Settings` -> `SublimeTmpl` -> `Settings - Default` 并在对应位置加入
>
"md": {
    "syntax": "Packages/MarkdownEditing/Markdown.tmLanguage",
    "extension": "md"
},

### Sublime w/ Evernote
1. 安装 **Evernote** 插件
2. 从 [印象笔记](https://app.yinxiang.com/api/DeveloperToken.action) 获取 Developer Token 和 NoteStore URL
3. 进入 `Preferences` -> `Package Settings` -> `Evernote` > `Settings - User` 并加入
>
{
    "token": \"***your token***\",
    "noteStoreUrl": \"***your NoteStore URL***\"
}
4. 进入 `Preferences` -> `Key Bindings` 中，在 User 配置文件中加入
>
{ "keys": ["ctrl+alt+e"], "command": "show_overlay", "args": {"overlay": "command_palette", "text": "Evernote: "} },
{ "keys": ["ctrl+e", "ctrl+s"], "command": "send_to_evernote" },
{ "keys": ["ctrl+e", "ctrl+o"], "command": "open_evernote_note" },
{ "keys": ["ctrl+e", "ctrl+u"], "command": "save_evernote_note" },
5. `ctrl + e, ctrl + s` 指先按 <kbd>ctrl</kbd> <kbd>e</kbd> 再按 <kbd>ctrl</kbd> <kbd>s</kbd>

## Usage
+ <kbd>ctrl</kbd> <kbd>shift</kbd> <kbd>p</kbd> -- open command palatte, support fuzzy matching (only initials)
+ <kbd>ctrl</kbd> <kbd>p</kbd> -- open file by name
+ <kbd>ctrl</kbd> <kbd>r</kbd> -- search function
+ <kbd>ctrl</kbd> <kbd>d</kbd> -- 多处同步编辑，<kbd>ctrl</kbd> <kbd>d</kbd> 后双击选择文本，继续 <kbd>ctrl</kbd> <kbd>d</kbd> 会追加选中所有相同文本
+ <kbd>shift</kbd> <kbd>rmb</kbd> -- 垂直选中
+ <kbd>ctrl</kbd> <kbd>shift</kbd> <kbd>f</kbd> -- 全文件查找