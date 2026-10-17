# 🏠 GoldenTellus FDE Community

> 我们不培养六边形战士。
> FDE 不是一个角色，是一条流水线。
> 这个仓库是 GoldenTellus Organization 的总入口，也是知识库和案例库的所在地。

在线站点：https://goldentellus.github.io/goldentellus-home/

## 🚦 有需求？从这里直达

| 你现在要做什么 | 推荐路径 |
|---|---|
| 我是企业，想判断 AI 项目是否值得做 | 🏢 [企业入口](./docs/for-enterprise.md) → 📚 [案例库](./docs/cases/index.md) |
| 我是新人，想知道从哪里学起 | 🌱 [新人入口](./docs/for-beginner.md) → 🧭 [流水线基础](./docs/knowledge/00-pipeline-fundamentals/index.md) |
| 我想理解一个 AI 落地问题 | 📚 [案例库](./docs/cases/index.md) → 🧠 [知识库](./docs/knowledge/index.md) |
| 我想深入某个工位 | 🔧 [FDE 入口](./docs/for-fde.md) → 🧠 [知识库](./docs/knowledge/index.md) |
| 我想参与讨论、组队或活动 | 🤝 [goldentellus-community](https://github.com/GoldenTellus/goldentellus-community) |
| 我想贡献文章或案例 | 🤝 [贡献指南](./docs/CONTRIBUTING.md) → 🗂️ [仓库与内容导航](./docs/navigation.md) |

## 🔁 一条完整的 FDE 路线

```text
🧭 找到工位
   ↓
🧠 学习岗位方法
   ↓
📚 阅读脱敏案例，理解约束
   ↓
🧪 用最小 Demo 验证方案
   ↓
🤝 在社区讨论、协作和持续迭代
```

你可以从任何一站开始，再沿着上游补知识、沿着下游做验证。

## 🗂️ 仓库结构

```text
docs/
├── index.md            # 站点首页
├── for-*.md            # 新人 / FDE / 企业入口
├── navigation.md       # 仓库与内容导航
├── knowledge/          # 知识库，按工位分目录（00-07、99）
└── cases/              # 案例库，正文在 by-industry/<industry>/
```

本地预览：

```bash
pip install mkdocs-material
mkdocs serve
```

推送到 `main` 后由 GitHub Actions 构建（`mkdocs build --strict`）并部署到 Pages。

## 📌 使用原则

- 案例必须有来源、授权状态、脱敏说明，并区分事实、估算和推断。
- Demo 不提交 API Key、客户原始数据、个人敏感信息或未经授权的第三方资产。
- 知识与案例目前都在本仓库；内容积累到一定规模后再拆分为独立仓库。
