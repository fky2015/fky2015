# AGENTS

## 仓库协作约定

- 这个仓库的主分支由我先维护静态内容，再由 bot 在其上动态更新。
- 这里的 `main` 指主分支。

## 人工更新基线

- 需要只查看、整理或继续维护人工内容时，应以 `user-only-updates` 为基线。

## 合并规则

- 不要通过 merge commit 的方式把 `user-only-updates` 合并到 `main`，否则 bot 提交仍会出现在 `main` 的历史里。
- 每次同步到 `main` 时，应直接将 `main` 重写到 `user-only-updates` 的最新提交。
- 不要把 bot 生成的提交当作必须保留的真实内容来源。
- `main` 的最终结果应以人工维护的内容为准，bot 只负责在其上重新生成动态部分。
- 推送到远端时，应使用 `git push --force-with-lease origin main` 更新 `origin/main`。
- 如果 bot 内容需要继续存在，应在人工内容合并完成后，再由 bot 基于最新的 `main` 重新生成。
