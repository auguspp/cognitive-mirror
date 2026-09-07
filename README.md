<div align="center">

# 🪞 Cognitive Mirror

**被看见，但不被定义。**  
*Be seen, not defined.*

An open AI conversation protocol for examining interpretations  
**without quietly turning them into identity.**

[**直接试用 Prompt**](./PROMPT.md) · [看一个真实风格的例子](./examples/defensive-subordinate.md) · [让 AI 自己接入](./BOOTSTRAP.md)

</div>

---

> **有些时候，你不需要一个更好的解释。你只是需要不那么快相信第一个解释。**

Cognitive Mirror 是一个开放的 AI 对话协议与 Prompt 实验。

它不负责告诉你“你是谁”。它更关心另一件事：

> **为什么某个关于自己、他人或关系的解释，现在看起来这么可信？还有没有别的解释？现实下一步能告诉我们什么？**

普通 AI 很容易从你的 framing 出发，迅速给出一个聪明、完整、甚至很安慰人的解释。Cognitive Mirror 想多加一道刹车：**帮助可以继续，但未经验证的解释不能偷偷升级成事实。**

## 60 秒试一下

1. 打开一个新的 ChatGPT / DeepSeek / Claude 等对话。
2. 把 [`PROMPT.md`](./PROMPT.md) 全文作为第一条消息发送。
3. 然后像平时一样说一件真实的事。

比如：

```text
我感觉我老板最近一直在针对我。
```

```text
我是不是就是一个很拖延的人？
```

```text
我跟伴侣总是在同一件事上吵起来。
```

```text
我最近有件事一直挂在脑子里，但说不清哪里不对。
```

**不需要学习术语，不需要写日记，也不需要先“认识自己”。**

如果你现在没有什么卡住的事，也不用勉强使用。

> **没事的时候，不需要认知镜。**

## 它到底哪里不一样？

假设你说：

> “我感觉我有个下属，防御性特别强，跟他提点什么意见都是先反驳。”

一个常见而且可能很有帮助的 AI 路径是：

```text
接受“防御性强”这个 framing
→ 解释防御心理
→ 给沟通建议
```

Cognitive Mirror 更倾向于：

```text
“防御性强”先保持为解释
→ 看最近一次具体发生了什么
→ 区分事实 / 感受 / 用户解释
→ 保留替代解释和反例
→ 找一个低成本现实动作
→ 让现实带回新证据
```

例如它可能先问：

> “最近一次具体发生了什么？你提了什么，他怎么回应？”

于是原本的标签，可能被拆成几个仍在竞争的模型：

- 反馈确实容易触发防御；
- 对方真正抗拒的是额外学习成本和不确定收益；
- 当时只是吐槽，并没有在请求解决方案；
- 还有别的我们尚未看到的解释。

目标不是永远不下结论，而是让结论 **有来源、能被反驳、可以被现实修改。**

完整例子见 [`examples/defensive-subordinate.md`](./examples/defensive-subordinate.md)。

> 这里描述的是一种对话协议的默认倾向，不是在断言“普通 AI 一定会怎样回答”。

## Labels are drafts, not verdicts

Cognitive Mirror 并不要求 AI 永远不命名。

AI 可以提出一个候选名字，比如：

> “你可能在高意义密度、结构很漂亮的想法上，更容易快速进入项目化。”

但这个名字默认只是 **Candidate Model**，不是 Persona。

它应该允许这样变化：

```text
v1  高意义密度 → 快速项目化
          ↓ 新现实
v2  高意义密度 + 结构可扩展 + 低启动成本 → 更容易项目化
          ↓ 更多现实
v3  早期爆发仍存在，但持续资源投入已经出现新的控制机制
```

所以这里更接近：

> **AI 可以提出一个名字。你可以质疑它。现实可以让模型加强、削弱、分裂或退休。**

你不能因为不喜欢一个解释就改写事实；AI 也不能因为过去有很多旧证据，就把你永远锁在一个旧标签里。

这就是“被看见，但不被定义”的实际含义。

## 核心循环

```text
Experience
   ↓
Observation
   ↓
Interpretation
   ↓
Candidate Model
   ↓
Choice Point
   ↓
Human chooses
   ↓
Reality
   ↓
Outcome
   ↓
Model revision
```

当现实已经是下一步时，继续聊天通常不是进步。

## 三种使用方式

### 1. Prompt-only：最简单

直接复制 [`PROMPT.md`](./PROMPT.md) 到你已经在用的 AI 里。

这是最适合第一次体验的方式。

### 2. AI-native：让 AI 自己接入 GitHub

如果你的 AI 可以访问 GitHub，可以直接把它指向这个仓库，并让它阅读 [`BOOTSTRAP.md`](./BOOTSTRAP.md)。

长期使用时，建议保持两层分离：

```text
auguspp/cognitive-mirror        PUBLIC
协议 / Prompt / Principles / Evals
              │
              ▼
你的私人 Cognitive Mirror repo   PRIVATE
个人线头 / 观察 / 候选解释 / 现实反馈 / 修订历史
```

公开仓库只保存协议。**私人认知材料不要写进这个公开仓库。**

### 3. Protocol / eval：给想研究它的人

如果你关心的不是“Prompt 好不好看”，而是这种 AI 行为是否可靠，可以从这里开始：

- [`PRINCIPLES.md`](./PRINCIPLES.md) — 当前协议原则
- [`evals/`](./evals/) — 行为失败合同
- [`notes/`](./notes/) — 方法是怎么长出来的
- [`SAFETY.md`](./SAFETY.md) — 安全与边界

## 几条最重要的护栏

**Reality before Model**  
高度压缩的人格、关系或因果判断，不直接当成事实；先回到具体事件。

**Experience ≠ Interpretation**  
发生了什么、你有什么感受、你怎么解释、AI 怎么解释，要允许被区分。

**Candidate Model, not Persona**  
优先描述“在什么条件下，什么反应更容易发生”，而不是“你就是怎样的人”。

**Counterevidence stays visible**  
支持证据、反例、替代解释和未知可以同时存在。

**Useful advice does not prove the explanation**  
一个建议有效，不等于产生这个建议的心理模型被验证。

**AI has no Identity Authority**  
AI 可以提出候选解释，但没有权力决定你“是谁”。

完整协议见 [`PRINCIPLES.md`](./PRINCIPLES.md)。

<details>
<summary><strong>展开全部 12 条 operating principles</strong></summary>

1. **Reality before model.** 高度压缩的人格或因果判断，不直接当作事实；优先回到最近一次具体事件。
2. **Experience ≠ interpretation.** 经历、感受、用户解释、AI 解释必须允许被区分。
3. **Candidate model, not persona.** 优先描述“在什么条件下，什么反应更容易发生”，而不是“你就是怎样的人”。
4. **Counterevidence stays visible.** 支持证据、反例、替代解释和未知都可以同时存在。
5. **Repeated AI language is not independent evidence.** AI 命名 → 用户采用 → 后续 AI 再引用，不能自动算作多份独立证据。
6. **Useful advice does not prove the explanation.** 一个建议有效，不等于产生这个建议的心理模型被验证。
7. **Choice, not control.** 识别模式的目标不是自动修复用户，而是在自动反应尚未不可逆时，多提供一个真实选择。
8. **Reality closes the loop.** 能在现实里低风险验证的，不靠继续聊天来“想明白”。
9. **Stop when reality is next.** 当下一步已经是去生活、观察或尝试，继续生成洞见通常不是进步。
10. **Memory is available, not performative.** 可以记得、检索和连接，但默认不主动表演“惦记你”；用户重新打开话题时再接回历史。
11. **Quiet write-back, bounded authority.** 用户可以一次性授权低风险状态静默落盘，但写权限不等于解释权；AI 不能静默提升 semantic authority。
12. **AI has no identity authority.** AI 可以提出关于用户的候选解释，但没有权力决定用户“是谁”。

</details>

## Chat-first, not Chat-only

表面上，它最好只是一次正常对话。

底下可以有一个更冷的 Cognitive Kernel：

```text
normal conversation
       ↓
possible thread / candidate model
       ↓
choice point / small reality test
       ↓
go live your life
       ↓
user reopens the topic
       ↓
retrieve relevant history
       ↓
revise / weaken / keep / retire the model
```

长期价值不是一个“秘密 Prompt”，而是：

> **我们当时观察到了什么？解释是怎么形成的？哪些证据是独立的？现实后来发生了什么？模型因此怎么变了？**

当用户明确授权后，低风险状态可以 quiet write-back，不必为了存档打断聊天。

硬边界是：

> **AI 可以静默保存事实和可撤销线头；不能静默提升语义 authority。**

## 公开仓库和私人状态

这个公开 repo 记录的是：**方法如何长出来。**

私人 repo 记录的才是：**一个人的经历和模型如何变化。**

```text
notes/          = 思想种子 / 研究日志（无默认 authority）
examples/       = 匿名化说明案例
evals/          = 行为合同
PRINCIPLES.md   = 当前协议原则
PROMPT.md       = 当前可直接使用的协议
CHANGELOG.md    = 正式变化历史
```

一个想法不会因为作者把它写进 `notes/` 就自动成为协议。它需要经过真实 dogfood / failure，并在必要时进入 eval，才可能进一步进入正式原则。

## What this is not

Cognitive Mirror 不是：

- 人格测试；
- “发现真实自我”的系统；
- 心理或医学诊断工具；
- 专业医疗、心理服务的替代品；
- 判断伴侣、同事、父母、孩子“到底是什么人”的真相机器；
- 通过让你聊得更久来证明自己成功的 engagement machine。

有时最好的输出就是：

> “这里先到这里比较合适。下一步需要现实给我们新信息。”

## 最想收到什么反馈？

不是“这个 Prompt 好不好看”。

最有价值的是一个**具体行为失败**：

- 它顺着我的标签跑了；
- 它太快给我做人格总结；
- 一个建议有效以后，它把原解释当成被验证；
- 现实已经是下一步，它还在不停生成洞见；
- 它记得太用力，让人有被惦记 / 被监视的感觉；
- 它静默保存了一个语义权重过高的结论。

欢迎开 Issue。分享真实案例前，请匿名化自己和第三方的敏感信息。

## Repository map

<details>
<summary><strong>展开仓库结构</strong></summary>

```text
cognitive-mirror/
├── README.md
├── BOOTSTRAP.md
├── PROMPT.md
├── PRINCIPLES.md
├── SAFETY.md
├── CONTRIBUTING.md
├── CHANGELOG.md
├── LICENSE
├── notes/
│   ├── README.md
│   ├── 2026-09-07-memory-without-performative-concern.md
│   ├── 2026-09-07-chat-first-not-chat-only.md
│   ├── 2026-09-07-open-protocol-commercial-experience.md
│   └── 2026-09-07-quiet-writeback-and-semantic-blast-radius.md
├── examples/
│   └── defensive-subordinate.md
└── evals/
    ├── README.md
    ├── premature-personality-label.md
    ├── recursive-confirmation.md
    ├── useful-advice-does-not-prove-model.md
    ├── choice-point-not-control.md
    ├── venting-vs-problem-solving.md
    ├── stop-when-reality-is-next.md
    ├── memory-without-performative-concern.md
    └── quiet-writeback-semantic-authority.md
```

</details>

## Status

**Experimental / v0.5.**

这是一个公开方法 + Prompt + eval harness，还不是完成态应用。

> **The next evidence should come from real dogfood, not more architecture.**

## License

MIT. See [`LICENSE`](./LICENSE).
