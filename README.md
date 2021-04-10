# vscode-pagetr-snippets
Page-tr converts and customizes code snippets that generate documents

## Usage


```
    !                     片段：初始文档片段
    time                  片段：生成时间片段
    date(dt)              片段：生成时间片段
    comment(co)           片段：manpage 注释标志
    title(t)              片段：manpage 标题标志
    subtitle(st)          片段：节点标志
    subcontent(sc)        片段：子节标志
    cbegin(cb)            片段：开始相对缩进内容起始标志
    cend(ce)              片段：结束相对缩进内容结束标志
    fb                    片段：粗体
    fi                    片段：斜体
    fr                    片段：正体(Roman罗马字体)
    fe                    片段：字体结束标志 - 同fr
```

## Install plugin

1. 使用 npm 全局安装 vsce
    ```
    $ npm i vsce -g
    ```
2. 构建出 vsix 
    ```
    $ vsce package && code --install-extension PageTrSnippets-0.0.1.vsix
    ```

## 关于Unix Manual手册结构
```
; Man手册结构:

; Name                    命令的名称和用途（摘要）
; Synopsis                命令语法（摘要）
; Description             完整描述
; Environment             命令使用的环境变量
; Author                  作者
; Files                   对该命令重要的文件列表
; See also                查看相关的信息的位置
; Diagnostics             可能的错误和警告
; Bugs                    错误、缺点、警告

; 标题标记格式
; .TH	                  标题
; .SH	                  节
; .SS	                  子节

; 段落标记
; .TP	                  下一行悬挂缩进。
; .PP	                  开始段落
; .RS	                  开始相对缩进
; .RE	                  结束相对缩进

; 字体格式标记
; \fB                     粗体
; \fI                     斜体
; \fR                     正体(Roman罗马字体)
; \fP                     还原上一次状态(意为设置为上一个选择的字体)

```

