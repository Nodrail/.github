# Agent Policy Format

APF is an open YAML format for AI agent permissions, maintained by Nodrail. Keep rules alongside your code and test what an agent may do before wiring the decision into its tool calls.

| If you want to…                                           | Start here                                                                                                                        |
| --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Try a policy locally and connect it to Claude Code        | [Local quickstart](https://nodrail.com/docs/quickstart)                                                                           |
| Use the evaluator in your own harness                     | [Library guide](https://nodrail.com/docs/library)                                                                                 |
| Implement compatible policy decisions                     | [Evaluator test cases](https://github.com/Nodrail/nodrail-js/blob/main/packages/policy-engine/tests/fixtures/conformance-v1.json) |
| Connect Claude Code or Codex to shared workspace policies | [Cloud plugins](https://github.com/Nodrail/agent-plugins)                                                                         |

The [engine and TypeScript client](https://github.com/Nodrail/nodrail-js) are available under Apache-2.0. [Nodrail Cloud](https://nodrail.com/pricing) provides shared approvals and decision history for teams. See each repository’s `SECURITY.md` for private vulnerability reporting.
