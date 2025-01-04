
---
title: Kodama 编译指令
author: kokic
date: 2025-1-4
---

指令 `kodama compile` 或缩写为 `kodama c` 将输入的 Markdown 文件构建成 HTML 文件. 

```
$ kodama c --help
Compiles an input markdown file into HTML format

Usage: kodama.exe compile [OPTIONS] <INPUT>

Arguments:
  <INPUT>  Path to input Typst file

Options:
  -o, --output <OUTPUT>  Path to output dir [default: ./publish]
  -r, --root <ROOT>      Configures the project root (for absolute paths) [default: ./] 
  -h, --help             Print help
```
