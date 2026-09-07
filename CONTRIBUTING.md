# Contributing

The most valuable contribution right now is **a real failure case**, not a new framework.

## Good issue material

Please share an anonymized example where the prompt:

- accepted a personality label too quickly;
- over-agreed with the user;
- invented motives for another person;
- treated repeated AI language as independent evidence;
- ignored an important counterexample;
- confused useful advice with proof of a model;
- kept analyzing after reality was clearly the next step;
- became too cold, clinical, or annoying;
- offered so many alternatives that it became useless;
- turned a Choice Point into covert behavioral control.

## Suggested report format

```text
Prompt version:
Model / provider:
User input (anonymized):
Assistant output:
What felt wrong:
What happened in reality afterward, if known:
```

Please remove names, employers, locations, contact details, private health information, and other identifying information about third parties.

## Design rule

Do not add schema, terminology, or policy merely because it sounds rigorous.

Prefer:

> observed failure → smallest rule or eval that prevents recurrence

over:

> interesting concept → new framework
