# wechat-html-v13

微信公众号文章 HTML 排版 Claude Code Skill（v13）

## 功能

将 Markdown / 纯文本文章转为微信公众号兼容的内联样式 HTML。

- **智能风格匹配**：AI 分析文章题材、情感基调、内容类型，从 20+ 风格族中自动推荐最佳排版
- **高分模板优先**：内置审美评分体系，同等条件下优先选用视觉效果更好的模板
- **纯内联样式**：所有 CSS 写在 `style=""` 属性上，完全兼容微信后台
- **即粘即用**：输出 HTML 直接复制粘贴到微信公众号编辑器

## 支持的风格族（20+）

| 风格 | 适用场景 | 审美评分 |
|------|----------|---------|
| 爱马仕风 (S) | 高端生活、精致内容 | 92 |
| Apple News (L) | 科技产品、APP评测 | 91 |
| Stripe Blog (M) | 技术教程、开发者内容 | 89 |
| 包豪斯 (Q) | 功能展示、几何设计 | 88 |
| 瑞士国际 (R) | 品牌宣传、正式场合 | 87 |
| Flipboard (G) | 专访、深度内容 | 86 |
| Medium (J) | 书评、长文阅读 | 85 |
| NYT (K) | 新闻资讯、权威报道 | 83 |
| 中式复古 (A1) | 历史、文化 | 68 |
| 温暖情感 (D) | 情感、育儿、故事 | 70 |
| … 及更多 | | |

## 安装

将本仓库克隆到 Claude Code skills 目录：

```bash
git clone https://github.com/YOUR_USERNAME/wechat-html-v13.git ~/.claude/skills/wechat-html-v13
```

然后在你的项目 `CLAUDE.md` 中引用：

```markdown
## Skills
@~/.claude/skills/wechat-html-v13/SKILL.md
```

## 使用方法

在 Claude Code 中直接说：

```
排版这篇文章：/path/to/article.md
```

或：

```
用v13排版 /path/to/article.md
```

Claude 会：
1. 分析文章特征，推荐 Top 3 风格
2. 确认后生成完整 HTML
3. 输出可直接粘贴到微信后台的代码

## 文件结构

```
wechat-html-v13/
├── SKILL.md      # Claude Code skill 定义
├── prompt.md     # v13 完整排版规范（风格定义 + 匹配系统）
└── README.md     # 本文件
```

## 提示词版本

当前：**v13**（高分模板优先 + 全球知名排版风格）

包含风格：中式复古、欧式复古、严谨商务、互联网年轻、清新自然、温暖情感、简约中性、潮流娱乐、Flipboard、原木Muji、蒙德里安、Medium、NYT、Apple News、Stripe、Substack、Notion、Bloomberg、包豪斯、瑞士国际主义、爱马仕、及多款配色变体。
