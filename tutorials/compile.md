
---
title: Kodama 编译指令
author: kokic
date: 2025-1-4
---

指令 `kodama compile` 或缩写为 `kodama c` 将输入的 Markdown 文件构建成 HTML 文件. 
尽管有 `--root` 参数, 但仍然建议所有用户在 `index.md` 文件所在的目录下执行 `kodama c`. 

```
$ kodama c --help
Compiles an input markdown file into HTML format

Usage: kodama.exe compile [OPTIONS] <INPUT>

Arguments:
  <INPUT>  Path to input Typst file

Options:
  -b, --base <BASE>      Base URL or publish URL (e.g. https://www.example.com/) [default: /]
  -o, --output <OUTPUT>  Path to output dir [default: ./publish]
  -r, --root <ROOT>      Configures the project root (for absolute paths) [default: ./] 
  -h, --help             Print help
```

对于当前这个网站的构建来说, 由于最终部署到的 URL 为 <https://kokic.github.io/echo>, 并非该域名的根目录, 为了保证生成链接的正确性, 用户应该指定 `--base` 这一编译参数, 即

```sh
kodama c index.md -b=https://kokic.github.io/echo/
```

当然, 如果用户只是在本地使用, 就不必考虑这个问题了. 
