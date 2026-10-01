# LoopEva 官网项目上下文

## 项目定位

- 本仓库是 **LoopEva 公司的官方网站**，对应 GitHub 仓库 [`LoopEva/LoopEva.github.io`](https://github.com/LoopEva/LoopEva.github.io)。
- 本地工作目录是 `/Users/xiuwei/Desktop/study/cv/LoopEva.github.io`。
- 官网的具体内容、视觉风格、信息架构和技术栈尚未确定；在用户明确方向前，不要自行定稿品牌文案或视觉语言。
- 当前仓库刚建立，尚未形成初始网站实现。后续开发默认都在本目录中进行。

## 公司背景（启动级理解）

LoopEva 的核心方向是让机器人在真实环境中持续完成任务并不断改进，重点围绕两条相互支撑的能力线：

- **Agentic Loop / LoopFoundry**：将机器人策略部署到真实环境，用 agent 负责任务编排、监测、恢复、人工升级和数据回流，形成真实世界的数据与学习闭环。
- **DexCore**：面向灵巧手、触觉和 steerable physical policy，拓展机器人可调用的物理能力，为更复杂的操作任务提供能力基础。

这段内容只是帮助接手项目的 agent 建立方向感，不是最终对外宣传文案。对外内容应以用户后续确认的公司叙事、产品边界和事实为准；不要把内部路线、人员安排、融资、排期或飞书文档内容直接写入网站。

## 公司背景参考

需要了解更多背景时，优先查看本机的 AI4Learn 公司资料：

- [公司资料索引](../../AI4Learn/company/index.md)
- [创业主线与技术 thesis](../../AI4Learn/company/startup.md)
- [当前状态快照](../../AI4Learn/company/current-state.md)
- [公司原始资料索引](../../AI4Learn/company/docs-map.md)
- [AI4Learn 总体接管说明](../../AI4Learn/Agents.md)

这些文件是内部工作资料，部分状态可能过期或包含不适合公开的内容。引用其中信息制作网站内容前，应先确认事实是否仍然有效、是否适合对外发布。公司实时执行信息仍以对应的飞书原件为准，不在本仓库复制内部文档。

## GitHub 与 Git 工作流

- 远程仓库：`git@github-loopeva:LoopEva/LoopEva.github.io.git`
- GitHub 页面：[https://github.com/LoopEva/LoopEva.github.io](https://github.com/LoopEva/LoopEva.github.io)
- 默认分支：`main`
- SSH Host 别名：`github-loopeva`
- 本机使用 LoopEva 专用 SSH 身份；不要读取、提交或传播 SSH 私钥、访问令牌或其他凭据。
- 本仓库已设置局部提交身份 `LoopEva`；不要为了本项目修改全局 Git 身份。

常用命令：

```bash
cd /Users/xiuwei/Desktop/study/cv/LoopEva.github.io

# 查看本地状态和远程地址
git status
git remote -v

# 开始工作前同步 main；有未提交改动时先处理改动
git pull --ff-only origin main

# 提交并推送
git add .
git commit -m "Describe the change"
git push -u origin main
```

首次推送后，日常推送可直接使用 `git push`。如果远程出现其他人的提交，先执行 `git pull --ff-only origin main`；不要在未检查的情况下强制 push 或重写远程历史。

## 开发约定

- 先确认页面目标、受众、文案事实和视觉方向，再选择或调整技术实现。
- 保持改动局部、可回滚；不要无理由引入框架、依赖或生成大量模板代码。
- 不把公司内部资料、隐私信息、凭据或未确认的业务判断写进网站源代码。
- 修改后至少检查 `git diff`、本地页面能否正常运行，以及是否误加入构建产物、依赖目录或环境文件。
