# RFC: New Token Refresh Logic
## Problem
### Impact
### Proposed Solution
### Diagrams


- [ ] Update SDK
- [ ] Unit tests
- [x] Update API documentation

| Status | Meaning           | Client Behavior     |
|--------|-------------------|----------------------|
| 200    | OK                | Return data          |
| 401    | Token expired     | Refresh + retry      |
| 500    | Server error      | Retry after 500ms    |

> Why does this fail?

>> Because the token gets regenerated before the worker completes the batch.

<details>
  <summary>Full stack trace</summary>
SOMETHING HAPPENS
</details>
