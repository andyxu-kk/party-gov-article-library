# party-gov-article-library

党政优秀文章知识库构建 Skill（WorkBuddy / 企业微信 AI 助手）。

把人民日报、新华社、湖南日报等权威党政媒体的优秀文章，加工成可长期复用的「党政写作知识资产」：分析文章整体结构与小标题体系，结合用户金句偏好提炼可迁移表达，并整理为便于 AI 知识库检索的 Markdown 文本。

## 功能

- 判断文章最适合的知识库主类型（党建引领 / 基层治理 / 乡村振兴 / 文旅发展 / 文化建设 等 15 类）
- 提炼文章整体结构与小标题体系规律
- 结合 `references/金句偏好样本.md` 校准金句审美，提炼值得长期积累的原文金句
- 生成稳定的 Markdown 文件名与 Front Matter（标题 / 来源 / 日期 / 类型 / 关键词 / 适用场景 / 结构特征）
- 输出可直接入库的 Markdown 知识文件

> 本 Skill 的目标不是新闻摘要，而是把已筛选出的优秀文章加工成可复用的写作知识资产。

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
├── references/
│   └── 金句偏好样本.md            # 金句审美校准参考库
└── README.md
```

## 使用

向 AI 提供一篇党政媒体文章（全文 / 截图转写 / 链接），并说明希望「分析、收藏、入库」，即可触发本 Skill。若你明确标记了「哪些句子是金句」，会被视为最高优先级的审美校准样本。

## License

仅供个人 / 团队内部知识管理使用。
