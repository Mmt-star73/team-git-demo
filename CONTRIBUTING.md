# 小组协作规范

## 1. 分支约定

| 分支 | 用途 | 谁能直接推 |
| --- | --- | --- |
| `main` | 稳定版本，随时可用 | 禁止直接推，只能通过 Pull Request 合并 |
| `feat/<名字>-<内容>` | 新内容 | 本人 |
| `fix/<名字>-<问题>` | 修改错误 | 本人 |

```bash
git switch main
git pull
git switch -c feat/zhangsan-env-setup
```

## 2. 提交信息规范

格式：`<类型>: <一句话说明>（署名）`

- `docs:` 写文档
- `feat:` 加新内容
- `fix:` 修错误
- `chore:` 杂项（改配置等）

示例：`docs: 补充环境准备章节（张三）`

## 3. 推送前必做

```bash
git pull --rebase origin main   # 先同步主干最新内容
git push origin <你的分支名>     # 再推送
```

## 4. Pull Request 流程

1. 推送分支后，GitHub 页面会出现黄色提示条，点 **Compare & pull request**。
2. 标题写清楚改了什么，描述里 @ 一位组员做评审。
3. 至少 1 人点 **Approve** 后才能合并。
4. 合并后删掉远端分支，本地执行 `git switch main && git pull`。

## 5. 硬性纪律

- 不直接往 `main` 推。
- 一次提交只做一件事，方便回滚和评审。
- 不提交大文件、压缩包、生成物（已在 `.gitignore` 中屏蔽）。
- 每两周同步一次：所有人本地执行 `git pull`。
