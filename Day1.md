# 第一天执行计划：环境、HTML、Git 与博客骨架

日期：2026-08-05  
时间：11:30–22:00  
有效学习：8 小时  
硬截止：22:00

## 今天的完成标准

今天不是以“看了多少课程”为标准，而是要留下这些可验证成果：

- Node.js LTS 与 npm 能在新开的 PowerShell 中显示版本。
- Git 全局姓名、noreply 邮箱和默认分支已经配置并验证。
- `learning-log` 中保存本计划和当天学习日志。
- 在 `learning-log` 亲手完成一次 `branch → commit → push → Pull Request → merge`。
- 创建第二个公开仓库 `conyhair/my-blog`，本地项目必须放在 `Frontend-learning` 的外面，避免嵌套 Git 仓库。
- `my-blog` 具有总计划要求的完整目录结构；首页能直接在浏览器打开。
- 关闭课程后，亲手写出首页的第一版 HTML，不复制整份答案。

已经完成：`learning-log` 已初始化，`main` 已推送，远程地址为 `https://github.com/conyhair/learning-log.git`。

## 时间表

### 11:30–12:00｜环境收尾与 Git 全局配置（30 分钟）

1. 等 Node.js 安装完成后，关闭并重新打开 PowerShell。
2. 验证安装：

```powershell
node --version
npm --version
```

预期：两条命令都输出版本号；Node.js 应为当前 LTS。若仍提示找不到命令，先重开终端，再检查安装是否完成，不要重复安装多个版本。

3. 配置并验证 Git：

```powershell
git config --global user.name "conyhair"
git config --global user.email "conyhair@users.noreply.github.com"
git config --global init.defaultBranch main

git config --global --get user.name
git config --global --get user.email
git config --global --get init.defaultBranch
```

预期依次看到 `conyhair`、noreply 邮箱和 `main`。

4. 亲手提交本计划：

```powershell
cd C:\Users\Asus\Desktop\Frontend-learning
git status
git add Day1.md
git commit -m "docs: add day 1 plan"
git push
```

### 12:00–12:45｜午餐与离屏休息（不计入有效学习）

不要边吃边看教程。

### 12:45–14:15｜freeCodeCamp 新内容（90 分钟）

范围只包括：

1. `Computer Basics`
2. `Basic HTML`

规则：

- 登录账号，保证进度保存。
- 每完成一个小节，用一句中文解释它解决什么问题，保留英文技术术语。
- 记录至少 3 个容易混淆或出错的点。
- 14:15 到点即停；不为了“刷完”延长时间。
- 今天不进入 CSS、JavaScript、React，也不额外开启第二套课程。

### 14:15–14:30｜休息（不计时）

起身、喝水、离开屏幕。

### 14:30–15:30｜创建 `my-blog` 与完整骨架（60 分钟）

1. 在 GitHub 网页创建公开、完全空白的仓库 `my-blog`，不要勾选 README、`.gitignore` 或 LICENSE。
2. 在 `C:\Users\Asus\Desktop\my-blog` 创建本地项目。不要放进 `Frontend-learning`，否则会形成嵌套 Git 仓库。
3. 按总计划创建全部目录和文件：

```text
my-blog/
├── index.html
├── reviews.html
├── diary.html
├── todo.html
├── posts/
│   ├── first-book-review.html
│   ├── first-movie-review.html
│   └── first-diary.html
├── assets/
│   ├── css/styles.css
│   ├── js/main.js
│   ├── js/todo.js
│   └── images/
├── README.md
├── LICENSE
└── .gitignore
```

4. `LICENSE` 使用标准 MIT License，版权行写 `Copyright (c) 2026 conyhair`。
5. README 注明：代码采用 MIT License；文章和图片内容除非另行说明，不随代码授权。
6. 初始化本地仓库并连接远程，但此时可以先不提交：

```powershell
cd C:\Users\Asus\Desktop\my-blog
git init -b main
git remote add origin https://github.com/conyhair/my-blog.git
git remote -v
git status
```

### 15:30–15:45｜休息（不计时）

### 15:45–16:45｜关闭教程，独立写首页第一版（60 分钟）

关闭 freeCodeCamp 和课程提示，在 `my-blog/index.html` 中亲手完成：

- 正确的 HTML 文档基本结构、页面语言和页面标题。
- 页眉、导航、主要内容区和页脚。
- 一个主标题、一段介绍、一个文章列表或文章卡片。
- 指向 `reviews.html`、`diary.html` 和 `todo.html` 的真实链接。
- 一张带有合适 `alt` 的图片；暂时没有图片时可以先写清楚待办，但不能伪造无意义的 `alt`。

限制：

- 暂不做视觉设计，不写 CSS 动画。
- 暂不实现 JavaScript 或 Todo 功能。
- 独立尝试 15 分钟后仍卡住，才向 Codex 请求“一级提示”；不要直接索要完整页面代码。

验收：双击打开 `index.html`，页面可读，导航链接可点击；允许其他页面暂时只有基础 HTML 骨架。

### 16:45–17:00｜休息（不计时）

### 17:00–18:30｜Git 最小命令与首次 PR 演练（90 分钟）

在 `learning-log` 中执行：

1. 先理解并亲手运行 `git status`、`git log --oneline`、`git branch`。
2. 创建练习分支：

```powershell
cd C:\Users\Asus\Desktop\Frontend-learning
git switch -c day-1-log
```

3. 创建 `logs/2026-08-05.md`，至少写入：

- 今天的目标。
- 已完成事项。
- 一个遇到的问题。
- 当前的下一步。

4. 检查、提交并推送：

```powershell
git status
git add logs/2026-08-05.md
git status
git commit -m "docs: add day 1 learning log"
git push -u origin day-1-log
```

5. 在 GitHub 网页创建 Pull Request：base 为 `main`，compare 为 `day-1-log`。阅读 diff，确认只包含预期文件后创建并合并 PR，再删除远程分支。
6. 回到本地同步并删除本地分支：

```powershell
git switch main
git pull --ff-only
git branch -d day-1-log
git status
git log --oneline --graph --decorate -5
```

这一段结束时，要能用自己的话解释：工作区、暂存区、commit、本地分支、远程分支和 PR 分别是什么。

### 18:30–19:15｜晚餐与离屏休息（不计入有效学习）

### 19:15–21:15｜完善博客骨架并首次推送（120 分钟）

1. 为其余 HTML 文件补上基础文档结构、页面标题和一致的导航。
2. 检查相对链接：根目录页面与 `posts/` 内页面的路径不同，不要机械复制。
3. README 至少写明：项目目的、当前状态、目录结构、如何本地打开、下一步计划。
4. `.gitignore` 只加入真实需要忽略的本地文件，不复制不了解的大型模板。
5. 在浏览器打开首页，并逐个点击导航；打开开发者工具，确认没有明显的文件加载错误。
6. 自己审查首次提交：

```powershell
cd C:\Users\Asus\Desktop\my-blog
git status
git diff
git add .
git diff --cached
git commit -m "feat: create initial blog structure"
git push -u origin main
git status
```

验收：GitHub 仓库能看到完整结构；本地显示 `main` 正在跟踪 `origin/main`；工作区干净。

### 21:15–21:30｜休息（不计时）

### 21:30–22:00｜学习日志、最终提交与收尾（30 分钟）

更新 `learning-log/logs/2026-08-05.md`：

- 今天实际完成了什么。
- 至少 3 个新概念，用自己的话解释。
- 至少 1 个错误：现象、原因、解决过程。
- 哪一步仍不熟练。
- 明天开始后的第一个动作。

提交更新：

```powershell
cd C:\Users\Asus\Desktop\Frontend-learning
git status
git add logs/2026-08-05.md
git commit -m "docs: complete day 1 learning log"
git push
git status
```

最后检查两个仓库都没有意外文件、密钥、账号、真实住址、电话、证件信息或私人行程。

## 卡住时的规则

1. 同一问题先独立尝试 15 分钟，并记录报错原文。
2. 请求帮助时提供：执行了什么、预期什么、实际发生什么、完整错误信息。
3. 先要思路或一级提示，再要局部示例，最后才考虑完整答案。
4. 如果临时中断，在仓库根目录创建或更新 `NEXT.md`，只写三句话：做到哪里、目前问题、回来后的第一步。
5. 不补课、不熬夜。22:00 必须停止；未完成项顺延到第二天，不能牺牲复现和日志来制造“全部完成”的假象。

## 22:00 最终验收清单

- [ ] `node --version` 与 `npm --version` 均成功。
- [ ] Git 全局姓名、邮箱和默认分支验证正确。
- [ ] `Day1.md` 已由自己提交并推送至 `learning-log/main`。
- [ ] freeCodeCamp 完成今天的 90 分钟定时学习。
- [ ] 关闭教程后完成 60 分钟独立复现。
- [ ] `learning-log` 的 PR 已创建、检查、合并并同步回本地。
- [ ] `logs/2026-08-05.md` 包含错误记录和下一步。
- [ ] `conyhair/my-blog` 是独立公开仓库，目录结构完整。
- [ ] 博客首页可在浏览器打开，主要导航链接可点击。
- [ ] 博客已有首次提交并推送，两个仓库的工作区均干净。
- [ ] 没有提前学习 CSS、JavaScript、React、后端或数据库。

