# Risk-Based Validation

Choose checks that detect the likely failure mode.

| Risk | Useful checks |
| --- | --- |
| Text or dictionary change | touched-file lint, key parity, target locale render |
| Local UI behavior | component test, targeted type check, manual state verification |
| Shared hook or utility | focused unit tests plus affected package type check |
| API contract or cache change | contract test, query-key and invalidation review, integration test |
| Route or package migration | old/new deep links, build config, CI target, redirect and rollback check |
| Security-sensitive change | authorization boundary tests, negative cases, secret and log review |
| Release change | production build, smoke plan, observability and recovery rehearsal |

Start narrow. Broaden only when the affected surface or a failure demands it. Record skipped checks and residual risk.
