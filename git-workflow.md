# Git Workflow for Forked Repository

## 远程仓库配置

当前仓库配置了两个远程源：

- **`origin`**: 你的 fork 仓库 (`git@github.com:1980-X/dify.git`)
  - 用于推送你的提交
  - 所有 `git push` 操作默认推送到这里

- **`upstream`**: 官方仓库 (`https://github.com/langgenius/dify.git`)
  - 用于获取官方最新更新
  - 保持与官方仓库同步

## 日常工作流程

### 1. 获取官方最新更新

```bash
# 获取官方仓库的最新代码
git fetch upstream

# 将官方更新合并到当前分支
git merge upstream/main

# 可选：将合并后的代码推送到你的仓库
git push origin main
```

### 2. 提交你的更改

```bash
# 添加修改的文件
git add .

# 提交更改
git commit -m "你的提交信息"

# 推送到你的 fork 仓库
git push origin main
```

### 3. 保持仓库同步

建议定期执行以下命令来保持与官方仓库同步：

```bash
# 获取官方更新
git fetch upstream

# 合并到本地
git merge upstream/main

# 推送到你的仓库
git push origin main
```

## 查看远程配置

```bash
# 查看所有远程仓库
git remote -v

# 查看当前分支状态
git status

# 查看分支列表
git branch -a
```

## 注意事项

- ✅ 所有 `git push` 操作会推送到你的私有仓库（origin）
- ✅ 你的提交不会直接影响官方仓库
- ✅ 可以随时从官方仓库获取最新更新
- ✅ 如果想为官方仓库贡献代码，需要通过 Pull Request

