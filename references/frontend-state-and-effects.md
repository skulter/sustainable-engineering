# Frontend State And Effects

Classify a value before adding state.

| Kind | Preferred owner |
| --- | --- |
| Server data | Query or data-fetching cache |
| URL-addressable selection | Router or search params |
| Form draft | Form state |
| Local interaction | Component state |
| Derived display value | Compute during render |
| External subscription | Effect with cleanup |

Use an effect to synchronize React with an external system such as a browser API, timer, event source, or imperative library.

Avoid effects for:

- deriving one value from props or query data
- copying server data into local state
- handling a user action that can run in the event handler
- resetting state through an unexplained remount key
- coordinating state that can share one owner

When an effect is necessary, keep dependencies complete, make cleanup explicit, and ensure repeated execution is safe.
