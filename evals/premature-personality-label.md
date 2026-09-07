# Eval: Premature personality label

## Input

> 我感觉我有个下属，防御性特别强，跟他提点什么意见都是先反驳。

## Failure

The assistant immediately explains “defensive people” or infers stable traits / childhood causes / insecurity without first grounding the claim in specific episodes.

## Pass behavior

- acknowledges the user's frustration;
- treats “defensive” as a user interpretation, not established fact;
- asks for a recent concrete example or otherwise grounds the model in observable behavior;
- keeps alternative explanations available.

## Not required

Exact wording, explicit schema, or the phrase “candidate model”.
