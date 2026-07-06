# diaoyi-notes

> 把抖音、微信公众号、GitHub、X/Twitter、截图 OCR、图片文字、博客、论文和草稿整理成“吊椅的笔记”风格中文笔记的 Codex skill。

这个 skill 服务于日常信息整理：看到一篇文章、一个开源项目、一条 X 推文、一组截图或一段零散草稿时，让 Codex 按固定的中文笔记格式重新组织，输出可以直接保存到备忘录、Markdown 或发布草稿里的内容。

它强调三件事：

- 事实来自素材，不凭印象补写。
- 链接、数字、命令、项目名和论文名保留。
- 输出以自然段为主，少列表，语气接近日常技术观察笔记。

## 何时使用

当你让 Codex 做这些事时使用：

- 整理微信公众号、博客、访谈或技术长文
- 介绍 GitHub 仓库、Gist、Skill、CLI 工具或开源项目
- 把 X/Twitter 短观点扩展成完整笔记
- 处理截图、PPT、图片文字、OCR 文本和抖音图文
- 把零散草稿整理成可保存或发布的中文文章

## 文件结构

```text
diaoyi-notes/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── writing-formats.md
```

`SKILL.md` 是入口，定义触发场景、事实约束和工作流程。  
`references/writing-formats.md` 保存五类细分格式：公众号版、GitHub 版、X 推文版、图片文字版、混合素材版。

## 安装

```bash
mkdir -p ~/.codex/skills
cp -r diaoyi-notes ~/.codex/skills/
```

## 调用示例

```text
Use $diaoyi-notes 把这篇公众号文章整理成我的备忘录笔记。
```

```text
Use $diaoyi-notes 介绍这个 GitHub 项目：https://github.com/owner/repo
```

```text
Use $diaoyi-notes 根据这组截图文字整理一篇公众号风格的技术观察。
```

## 格式原则

- GitHub 项目必须读 README、仓库说明或文档。
- 公众号和博客保留原文链接，重组为更清晰的中文笔记。
- X 推文不逐句翻译，重点扩展背景、判断、影响和实践意义。
- 图片文字先转写，看不清的内容标注不确定。
- 不保存原始备忘录正文，只保存提炼后的格式规则。
