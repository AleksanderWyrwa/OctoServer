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
