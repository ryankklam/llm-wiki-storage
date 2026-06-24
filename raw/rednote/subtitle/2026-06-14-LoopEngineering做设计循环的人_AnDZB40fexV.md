# Loop Engineering：做设计循环的人

> 视频标题：Loop Engineering：做设计循环的人
> 作者：思享新境
> 小红书链接：http://xhslink.com/o/AnDZB40fexV
> 平台：小红书
> 日期：2026-06-14

---

## 什么是 Loop Engineering

[00:00] 你现在还在一条一条提示 Agent 吗？可能很快，这就不是主流工作方式了。真正的变化不是提示词写得更好，而是你开始设计一个系统。

[00:11] 这个系统自己发现任务，自己分发任务，自己检查结果。然后它再去提示 Agent。这不是换一种 Prompt 写法。

[00:21] 这是把提示这件事本身放进工程系统里。这就是 Loop Engineering，你可以把它理解成一个会自动执行的目标。

[00:30] 你定义目的，AI 一轮一轮推进，直到某个可验证的条件成立。人不再站在每一轮对话的正中间，人开始站到系统设计的位置上。

[00:40] 这件事听起来有点夸张，所以先别急着兴奋，现在还很早。

[00:45] Token 成本也非常现实。同一个 Loop，在 Token 充裕和 Token 紧张的团队里，可能完全不是一回事。

[00:53] 但这个方向值得认真看，因为它很可能改变我们使用 AI Agent 的方式。

[00:59] 它改变的不是某一次输出，而是你和 Agent 协作时，谁来决定下一步。

## 从手动 Prompt 到 Agent Loop

[01:05] 过去两年，我们使用 AI Agent 的方式很直接：你写一个 Prompt，你补一堆上下文，Agent 返回结果。

[01:13] 你看完，再写下一条 Prompt，一轮接一轮。Agent 是工具，你一直握着它。

[01:19] Loop Engineering 换了一个姿势：你不再亲自推动每一步，你构建一个小系统，它会发现工作，会把工作分出去，会检查结果，会记录做到了哪里，然后决定下一步该让哪个 Agent 做什么。

[01:34] 它和 Agent Loop 很像，但位置更高一层。

[01:38] Agent Loop 是单个 Agent 运行的环境。

[01:41] Multi-Agent 是构建软件的系统，Loop 则像一个会定时运行的 Agent Loop，它会拉起小助手，会读自己的状态，也会把输出重新喂回下一轮。

## 工具选择的变化

[01:52] 让我意外的是，这已经不太是工具选择的问题。以前你想做一个 Loop 可能要写一堆 Bash，然后堆一堆脚本永远归你维护。现在很多组件直接进了产品。

[02:04] Claude Code 有一套，Cursor 也有一套，名字不完全一样，但形状非常接近。所以重点不是按下某个按钮，重点是设计一个换了工具也还能跑的工作回路。

## Loop 的五个核心组件

[02:17] 一个 Loop 大概需要五个东西，再加一个记忆系统。

[02:21] 第一，Automations；第二，Worktrees；第三，Skills；第四，Plugins 和 Connectors；第五，Sub-Agents；第六，State，也就是状态记忆。这张清单不复杂，但少一个 Loop 就会露。

[02:36] 五个组件各管一件事：Automations 负责醒来，Worktrees 负责隔离，Skills 负责把项目知识写下来，Plugins 和 Connectors 负责连接真实工具，Sub-Agents 负责让写的人远离检查的人。

[02:51] State 要单独拎出来看：没有 Automations，它不会醒；没有 State，它会失忆；没有 Verifier，它会自信地错。这个 State 可以是 Markdown，可以是 Linear Board，也可以是 Agent 的 MB 或 Progress Files。

[03:07] Claude Code 和 Cursor 都有这些能力。Claude Code 有 Automations Tab，内建 Worktrees、Agent Skills、MCP Plugins、Sub-Agents。

[03:18] Cursor 有 Agents、Queues 和 Hooks、Git Worktree、Skills、MCP Service、Agent Teams。

[03:25] 名字不同，但能力本质上是同一批。先说 Automations，它是 Loop 的心跳。如果没有自动触发，那就只是你某天手动跑了一次。

[03:36] 有了 Automations，它才能每天、每小时，或者按你定义的节奏醒来。它去看 Issue，去看 CI，去看最近的 Commit，然后把值得处理的东西推到你面前。

[03:48] 在 Claude Code 里，你可以在 Automations Tab 里配置：选项目，写 Prompt，定 Cadence，决定它跑在本地 Checkout 还是后台 Worktree。有发现的结果进 Triage Inbox，没发现问题的运行自动归档。这种细节很小，但很关键。

[04:08] 因为它让重复检查变成系统行为。

[04:11] Cursor 则是 Scheduling 和 Hooks：你可以用 Loop 按严格跑，也可以设 Cron，可以用 Hooks 在 Agent 生命周期里触发命令，还可以把整套东西放进 GitHub Actions，这样你关掉电脑，它也能继续跑。

[04:26] 工具入口不同，目标一样。还有一个更关键的语义：Loop 是重复运行，Goal 是一直运行，直到条件真的满足。

[04:37] 比如你写"所有测试通过、Lint 干净"，Agent 每轮推进一点，每轮之后另一个模型检查有没有完成。写代码的不给自己打分。

### 组件二：Worktrees

[04:49] 第二个组件是 Worktrees。只要你让多个 Agent 同时干活，文件冲突就会马上出现——两个 Agent 改同一个文件。

[04:58] 这和两个工程师没沟通就改同一段代码，没有本质区别。

[05:03] Git Worktrees 的价值，就是给每个 Agent 独立的 Checkout。它们共享同一份历史，但彼此碰不到对方的工作区。

[05:13] Claude Code 把这个能力做进去了，Agent Thread 可以同时作用在同一个 Repo 上。Cursor 则可以用 Git Worktree、Worktree 或者给 Sub-Agent 配 Isolation Worktree。

[05:24] 这能解决机械冲突，但解决不了人的判断。你能跑多少 Agent，不取决于工具，取决于你能审阅多少东西。

[05:33] Worktrees 把文件分开，但它不会替你判断哪份改动值得合并。

### 组件三：Skills

[05:37] 第三个组件是 Skills。它解决的是另一个老问题：不要每次都重新给 Agent 解释项目。

[05:44] 一个 Skill 通常就是一个文件夹，里面有 SKILL.md、可能的 Scripts、Reference、Assets。

[05:53] 你把项目约定、构建步骤、踩坑经验写进去，Agent 每次运行时读取。

[05:59] 这件事其实是在对抗冷启动。Agent 每次会话都是冷启动，你没说清楚的地方，它会用猜测补上。

[06:08] Skills 就是把这些意图放到对话外面。比如：我们为什么不用某种库法？上线前必须跑哪些命令？哪类文件不能碰？

[06:18] 这些东西一旦写成 Skill，Loop 才不会每轮都从零推倒。

[06:23] 更重要的是，它让团队知识开始复用。

[06:26] 一次写下来的约定，下一轮还能用，下一个 Agent 还能用，下一个 Repo 也可能还能用。

### 组件四：Plugins 和 Connectors

[06:33] 第四个组件是 Plugins 和 Connectors。

[06:36] 如果一个 Loop 只能看文件系统，那它很小。

[06:40] 真实工作，通常分布在 Issue Tracker、数据库、Staging API、Slack 或者别的团队工具里。

[06:47] MCP Connectors 的意义，就是让 Agent 能接触这些真实工具，而不是只在 Repo 里猜。

[06:54] 这样 Loop 才能完成更完整的动作。比如，它发现一个问题，不只是写一个 Patch。

[07:00] 它可以打开 PR，关联 Linear Ticket，等 CI 变绿以后通知频道。

[07:05] 也可以把处理不了的事项丢回 Triage Inbox。

[07:09] 文件改动只是其中一步，工作流的收口也很重要。

### 组件五：Sub-Agents

[07:13] 第五个组件是 Sub-Agents。

[07:16] 它的关键不是多叫几个模型一起热闹，而是把 Maker 和 Checker 分开。

[07:21] 一个 Agent 负责探索问题，一个 Agent 负责实现修复，另一个 Agent 负责验证和挑错。

[07:28] 写代码的人不应该默认给自己的代码盖章。

[07:31] Claude Code 的 Sub-Agents 可以在 Claude Agents 里用 TOML 定义角色。

[07:37] Cursor 则可以用 Claude Agents 和 Teams。

[07:41] 你甚至可以给不同角色分配不同模型。

[07:44] 但这里也有成本判断。

[07:46] Sub-Agent 很有价值，但不应该到处乱花。

[07:50] 它更适合高风险改动、共享模块、生产发布，或者你明显不信任第一轮结果的时候。

## 一个完整的 Loop 长什么样

[07:57] 把这些拼起来，一个 Loop 就长这样。

[08:00] 每天早上，一个 Automation 在 Repo 上跑。

[08:03] 它调用一个 Triage Skill，先读昨天的 CI 失败、打开的 Issue、最近的 Commit。

[08:09] 也就是说，它不是凭空开始工作，它先读现场。

[08:14] 然后它把发现写下来，可以写进 Markdown，也可以写进 Linear。

[08:19] 遇到值得处理的问题，就开一个独立 Worktree。一个 Sub-Agent 起草修复，另一个 Sub-Agent 审阅。

[08:26] 这里重要的是：状态先落地，工作再分发。

[08:30] 否则你只是在并行制造更多需要合并的改动。

[08:33] 最后，Connectors 帮它收口：该开的 PR 打开，该更新的 Ticket 更新。

[08:40] CI 绿了以后，通知频道；处理不了的问题进入 Triage Inbox。State File 记住做过什么、通过什么、还剩什么。

[08:49] 这样明天早上，Loop 不是重来一遍，而是接着昨天继续跑。

## Loop 的风险与挑战

[08:53] 但 Loop 不会把你从工作里删除，它只是改变你站的位置。而且有三个问题会变得更尖锐。

[09:00] 第一个是验证责任。Agent 说"done"只是一个主张，不是证明。测试、Review、上线后的信号才是证据。

[09:09] 最后判断这件事能不能进主干，仍然是工程师责任。

[09:14] 第二个是认知距离。Loop 越快交付你没写的代码，你和系统之间的距离就越大。

[09:21] 第三个是渐进式放弃。当一个系统看起来能自己跑，人很容易停止判断。

[09:27] 你开始相信它的状态，相信它的总结，相信它说"已经完成"。这比单次错误更危险，因为它会慢慢改变你的工作习惯。

## 总结

[09:38] 所以结论不是不要 Loop。直接提示 Agent 仍然有效，很多任务也不需要完整 Loop。关键是平衡。

[09:50] Loop Engineering 比 Prompt Engineering 更难，因为关注点移动了。

[09:58] 你不再只是写一句提示词，而是在设计一个会持续运行、会分发工作、会记录状态、会被验证的系统。

[10:06] 构建 Loop，但继续做工程师。
