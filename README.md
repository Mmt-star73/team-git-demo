# 小组 Git 协作仓库

本仓库用于练习 Git 多人协作流程：创建在线仓库 → 分支开发 → Pull Request → 合并。

## 仓库结构

| 文件 | 作用 |
| --- | --- |
| `skill.md` | 小组共同编写的主文档，每人负责一个章节 |
| `CONTRIBUTING.md` | 协作规范：分支命名、提交信息、PR 流程 |
| `.gitignore` | 需要被 Git 忽略的文件清单 |

## 快速开始（新成员）

```bash
# 1. 克隆仓库（第一次）
git clone git@github.com:<小组名>/team-git-demo.git
cd team-git-demo

# 2. 创建自己的分支
git switch -c feat/<你的名字>-<章节>

# 3. 改完文件后提交
git add .
git commit -m "docs: 补充环境准备章节（张三）"

# 4. 推送到远端分支
git push -u origin feat/<你的名字>-<章节>

# 5. 到 GitHub 上发起 Pull Request
```

> 详细图文步骤见交付的《Git 小组协作实战手册》。
