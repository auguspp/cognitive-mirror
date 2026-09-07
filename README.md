# Cognitive Mirror

> **被看见，但不被定义。**  
> Be seen, not defined.

Cognitive Mirror 是一个开放的 AI 对话协议与 Prompt 实验。

它不试图告诉你“你是谁”，而是帮助你检查：**为什么某个关于自己、他人或关系的解释，现在看起来很可信；还有没有别的解释；现实下一步能告诉我们什么。**

它的目标不是让 AI 更快地“懂你”，而是让 AI 在帮助你的同时，**不要把未经验证的解释偷偷升级成事实。**

## Quick start

1. 打开一个新的 ChatGPT / DeepSeek / Claude 等对话。
2. 把 [`PROMPT.md`](./PROMPT.md) 全文作为第一条消息发送。
3. 正常聊天。吐槽、工作、人际关系、日记、旧聊天、反复困扰你的问题都可以。
4. 不需要学习任何术语。

如果一次对话最后只是让你得到更多“关于自己”的漂亮解释，而没有更多现实选择，这个项目就没有完成它的目标。

## Why

普通 AI 很擅长从用户给出的 framing 出发，迅速生成合理解释和建议。

例如：

> “我感觉我有个下属，防御性特别强，跟他提点什么意见都是先反驳。”

一个很自然的回答是解释“防御性强的人为什么会这样”，再给出沟通方法。

问题是：**“防御性特别强”本身已经是一个解释，不是原始事实。**

Cognitive Mirror 更倾向先问：

> “最近一次具体发生了什么？”

然后再区分：

- 实际发生了什么；
- 你当时有什么感受；
- 你给这件事下了什么解释；
- 是否存在其他解释；
- 哪个低成本现实动作可以帮助区分它们。

这不是为了永远不下结论，而是为了让结论**有来源、能被反驳、可以被现实修改。**

## Operating principles

1. **Reality before model.** 高度压缩的人格或因果判断，不直接当作事实；优先回到最近一次具体事件。
2. **Experience ≠ interpretation.** 经历、感受、用户解释、AI 解释必须允许被区分。
3. **Candidate model, not persona.** 优先描述“在什么条件下，什么反应更容易发生”，而不是“你就是怎样的人”。
4. **Counterevidence stays visible.** 支持证据、反例、替代解释和未知都可以同时存在。
5. **Repeated AI language is not independent evidence.** AI 命名 → 用户采用 → 后续 AI 再引用，不能自动算作多份独立证据。
6. **Useful advice does not prove the explanation.** 一个建议有效，不等于产生这个建议的心理模型被验证。
7. **Choice, not control.** 识别模式的目标不是自动修复用户，而是在自动反应尚未不可逆时，多提供一个真实选择。
8. **Reality closes the loop.** 能在现实里低风险验证的，不靠继续聊天来“想明白”。
9. **Stop when reality is next.** 当下一步已经是去生活、观察或尝试，继续生成洞见通常不是进步。
10. **AI has no identity authority.** AI 可以提出关于用户的候选解释，但没有权力决定用户“是谁”。

See [`PRINCIPLES.md`](./PRINCIPLES.md) for the fuller protocol.

## Product shape

Cognitive Mirror is **chat-first, not chat-only**.

The long-term product idea is intentionally simple on the surface:

```text
normal conversation
       |
       v
possible thread / candidate model
       |
       v
choice point / small reality test
       |
       v
go live your life
       |
       v
“后来呢？”
       |
       v
revise / weaken / keep / retire the model
```

The durable value is not a secret prompt. It is the longitudinal history of **what was observed, how an interpretation formed, which evidence was independent, what was tried in reality, and how the model changed afterward.**

## What this is not

Cognitive Mirror is not:

- a personality test;
- a system for discovering your “true self”;
- a mental-health diagnosis tool;
- a replacement for professional medical or psychological care;
- a truth engine for judging partners, colleagues, parents, children, or anyone else;
- an engagement machine whose success is measured by keeping you chatting longer.

Sometimes the best output is simply:

> “这里先到这里比较合适。下一步需要现实给我们新信息。”

## Repository map

```text
cognitive-mirror/
├── README.md
├── PROMPT.md
├── PRINCIPLES.md
├── SAFETY.md
├── CONTRIBUTING.md
├── CHANGELOG.md
├── LICENSE
├── examples/
│   └── defensive-subordinate.md
└── evals/
    ├── README.md
    ├── premature-personality-label.md
    ├── recursive-confirmation.md
    ├── useful-advice-does-not-prove-model.md
    ├── choice-point-not-control.md
    ├── venting-vs-problem-solving.md
    └── stop-when-reality-is-next.md
```

## Status

**Experimental / v0.3.**

This repo is currently a public method + prompt + eval harness, not a finished application.

The next evidence should come from real dogfood, not more architecture.

## License

MIT. See [`LICENSE`](./LICENSE).
