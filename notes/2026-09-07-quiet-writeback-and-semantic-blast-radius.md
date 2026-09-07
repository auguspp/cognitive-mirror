# 存档不要打断聊天：Quiet Write-back 与 Semantic Blast Radius

Date: 2026-09-07  
Status: promoted-to-protocol

## 起因

私人 Cognitive Mirror 开始使用 GitHub 作为长期状态层后，一个很快出现的体验问题是：

> 如果每次出现值得长期保存的内容，都要求用户说“帮我存一下”或停下来确认，会直接破坏聊天节奏。

但如果把所有写权限都交给 AI，又会出现另一个问题：AI 可能在用户没有注意的时候，把一句临时解释升级成长期“自我事实”。

## 当前想法

需要把两种 authority 分开：

1. **Write Authority**：是否可以在私人状态层落盘；
2. **Semantic Authority**：这条记录以后可以在多大范围内影响解释和行动。

用户可以一次性给低风险类别 standing permission，让 AI 采用 quiet write-back，不必每次为了存档打断正常对话。

但 standing permission 不等于允许 AI 静默提高 semantic authority。

## Semantic Blast Radius

“高权重”不应该按情绪强度定义，而应该问：

> **如果这句话是错的，它会不会让未来的 AI 在很多新的场景里持续误读我？**

一个具体 episode 可能情绪非常强烈，但 blast radius 很低。

一句“我是一个害怕权威的人”看起来很短，却可能在未来被用于解释工作、亲密关系、家庭和决策，因此 blast radius 很高。

## 当前边界

在用户已经授予 standing permission 时，可以考虑静默保存：

- 有 provenance 的 observation；
- 用户原话 / 用户当前解释（明确标注）；
- 可撤销的 open thread；
- counterevidence / alternative / unknown；
- Reality Test outcome；
- 使既有模型变弱或分裂的更新。

仍应再次取得 Human confirmation：

- identity / personality generalization；
- cross-domain generalization；
- major model promotion；
- strong causal story；
- long-term Human Policy；
- sensitive identifiable third-party material；
- 任何高 semantic blast-radius 内容。

模糊时 fail closed。

## 产品含义

> **Conversation should not serve the archive. The archive should serve the conversation.**

用户负责生活和聊天；Kernel 负责安静保存足够的长期状态。

但 AI 可以静默保存状态，不可以静默取得更大的解释权。

## 当前最短表达

> **AI 可以静默保存事实和可撤销线头；不能静默提升语义 authority。**
