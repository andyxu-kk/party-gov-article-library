# party-gov-article-library

党政优秀文章知识库构建 Skill（WorkBuddy / 企业微信 AI 助手）。

把人民日报、新华社、湖南日报等权威党政媒体的优秀文章，加工成轻量、可检索、可复用的「党政写作知识卡片」：提炼文章结构骨架与可迁移金句，整理为便于 AI 知识库检索的 Markdown 文本。

## 功能

- 判断文章最适合的知识库主类型（党建引领 / 基层治理 / 乡村振兴 / 文旅发展 / 文化建设 等 15 类）
- 提炼 1 行结构骨架 + 1—2 段结构说明（支持无小标题文章的隐性结构识别）
- 结合 `references/金句偏好样本.md` 校准金句审美，提炼值得长期积累的原文金句
- 生成精简 Front Matter（标题 / 来源 / 日期 / 类型 / 关键词 / 原文链接）
- 输出可直接入库的 Markdown 知识卡片（正文仅「文章结构 + 金句」两个板块）

> 本 Skill 的目标不是新闻摘要，而是把已筛选出的优秀文章加工成轻量、可复用、可直接调用的知识卡片。

> 原则：文件名负责找到它，关键词负责让 AI 搜到它，文章结构负责学框架，金句负责直接调用，除此之外能不写就不写。

## 安装

将本仓库克隆或解压到 WorkBuddy 的技能目录：

```bash
# 方式一：直接克隆
git clone https://github.com/andyxu-kk/party-gov-article-library.git ~/.workbuddy/skills/party-gov-article-library

# 方式二：从本地解压
# 把整个 party-gov-article-library 文件夹放到 ~/.workbuddy/skills/ 下即可
```

放入后，在 WorkBuddy 对话中输入 `/party-gov-article-library` 或在需要时由 AI 自动触发。

## 目录结构

```
party-gov-article-library/
├── SKILL.md                      # 技能主文件（工作流与标准）
├── config.example.json           # 知识库路径配置文件模板（复制为 config.json 后按本机修改）
├── .gitignore                    # 排除本机 config.json
├── references/
│   ├── 金句偏好样本.md            # 金句审美校准参考库
│   └── 文章链接抓取经验.md        # 文章链接抓取实战经验
└── README.md
```

## 知识库路径配置

本 Skill 不硬编码机器专属路径。新电脑安装后，如文章库路径与默认值不同，在 skill 目录下创建 `config.json`（参考 `config.example.json`）：

```json
{
  "library_path": "D:\\我的文档\\党政文章库"
}
```

目录解析优先级：用户当场指定 > 本机 `config.json` > 默认值。`config.json` 不会被提交到 GitHub。

## 使用

向 AI 提供一篇党政媒体文章（全文 / 截图转写 / 链接），并说明希望「分析、收藏、入库」，即可触发本 Skill。若你明确标记了「哪些句子是金句」，会被视为最高优先级的审美校准样本。

## License

仅供个人 / 团队内部知识管理使用。
