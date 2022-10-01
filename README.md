# 乱七八糟的模板 | Miscellaneous Templates

<center>

[![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/Zuoqiu-Yingyi/siyuan-template-misc?include_prereleases&style=flat-square)](https://github.com/Zuoqiu-Yingyi/siyuan-template-misc/releases/latest)
[![GitHub Release Date](https://img.shields.io/github/release-date/Zuoqiu-Yingyi/siyuan-template-misc?style=flat-square)](https://github.com/Zuoqiu-Yingyi/siyuan-template-misc/releases/latest)
[![GitHub License](https://img.shields.io/github/license/Zuoqiu-Yingyi/siyuan-template-misc?style=flat-square)](https://github.com/Zuoqiu-Yingyi/siyuan-template-misc/blob/main/LICENSE)
[![GitHub last commit](https://img.shields.io/github/last-commit/Zuoqiu-Yingyi/siyuan-template-misc?style=flat-square)](https://github.com/Zuoqiu-Yingyi/siyuan-template-misc/commits/main)
![GitHub repo size](https://img.shields.io/github/repo-size/Zuoqiu-Yingyi/siyuan-template-misc?style=flat-square)
![hits](https://hits.b3log.org/Zuoqiu-Yingyi/siyuan-template-misc.svg)
[![GitHub all releases](https://img.shields.io/github/downloads/Zuoqiu-Yingyi/siyuan-template-misc/total?style=flat-square)](https://github.com/Zuoqiu-Yingyi/siyuan-template-misc/releases)

</center>

思源笔记的一套乱七八糟的工具类模板  
A miscellaneous set of tool-like templates for Siyuan Notes.

## 预览 | PREVIEW

## 介绍 | INTRODUCTION

本套模板由三组模板组成  
This set of templates consists of three types of templates.
- `Query`: 查询工具 | query tools
  - 该组模板需要首先安装 `Query` 挂件  
    This group of templates requires the widget of `Query` to be installed first.
  - [Zuoqiu-Yingyi/widget-query: 一个将思源笔记数据库查询结果以表格样式渲染的挂件 | A widget that renders the query results of the Siyuan Notes database in tabular style.](https://github.com/Zuoqiu-Yingyi/widget-query)
  - 该组模板主要使用 `Query` 挂件实现一些查询功能  
    This group of templates primarily implements some query functions using `Query` widget.
- `Embed`: 嵌入工具 | embed tools
  - 该组模板主要使用嵌入块实现一些汇总功能  
    This group of templates primarily implements some summarization functions using embeded block.
- `Other`: 其他工具 | other tools
  - 该组模板主要实现其他功能  
    This group of templates primarily implements some other functions.

### 模板介绍

- `Query`
  - `查询今日更新的文档.md` | `query-updated-doc-today.md`
    - 以表格的形式汇总今日更新的文档 (排除挂件所在的文档)  
      Summarize today's updated documents in tabular form (excluding the documents where the widget is located).
    - `00:00 ~ 现在` | `00:00 ~ Now`
  - `查询24小时内更新的文档.md` | `query-updated-doc-24H.md`
    - 以表格的形式汇总 24 小时内更新的文档 (排除挂件所在的文档)  
      Summarize the updated documents within 24 hours in tabular form (excluding the documents where the widget is located).
- `Embed`
  - `汇总当前文档反链.md` | `sum-backlink-of-doc.md`
    - 以嵌入块的形式汇总当前文档的反链 (所有引用当前文档的块)  
      Summarize the backlink of the current document as an embedded block (all blocks that reference the current document).
- `Other`
  - `当前文档信息.md` | `doc-info.md`
    - 以表格的形式生成当前文档的信息  
      Render the information of the current document in tabular form.
      - 当前文档标题 | the title of the current document
      - 当前文档命名 | the name of the current document
      - 当前文档别名 | the alias of the current document
      - 当前文档备注 | the memo of the current document
      - 当前文档 ID | the ID of the current document
      - 当前文档路径 | the path of the current document
      - 当前文档创建时间 | the creation time of the current document
      - 当前表格更新时间 | the update time of the current document

## 更改日志 | CHANGE LOG

[CHANGE LOG](./CHANGELOG.md)
