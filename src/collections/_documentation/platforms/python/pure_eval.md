---
title: pure_eval
sidebar_order: 9
---

{% version_added 0.16.2 %}

This integration uses [`pure_eval`](https://github.com/alexmojaki/pure_eval) to safely evaluate additional expressions in the source code and display their values alongside other local variables.

**This integration is experimental.** It may be removed in minor versions.

Python version 3.5 or greater is required.

To install dependencies, either `pip install 'sentry-sdk[pure_eval]'` or `pip install pure_eval executing asttokens`.

Add ``PureEvalIntegration()`` to your ``integrations`` list:

```python
import sentry_sdk
from sentry_sdk.integrations.pure_eval import PureEvalIntegration

sentry_sdk.init("___PUBLIC_DSN___", integrations=[PureEvalIntegration()])
```