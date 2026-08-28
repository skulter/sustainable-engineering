# Maintainability Criteria

Use these questions to compare implementation choices.

- Intent: Can a developer explain the behavior without reconstructing hidden state?
- Ownership: Does each component, hook, service, or module own one coherent responsibility?
- Data flow: Is there one authoritative source for each value?
- Coupling: Can the behavior change without editing unrelated layers?
- Contracts: Are public inputs, outputs, errors, and lifecycle expectations explicit?
- Change cost: Does the design support the next known change without speculative generalization?
- Testability: Can important behavior be verified at the narrowest responsible boundary?
- Operations: Are failures observable and recovery paths understood?
- Conventions: Does the solution fit the repository unless deviation has a concrete benefit?
- Deletion: Can any state, effect, wrapper, abstraction, or branch be removed?

Prefer the option that is correct and easiest to explain. A shorter implementation is not automatically simpler.
