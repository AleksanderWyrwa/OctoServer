### Suggested Changes
- [ ] Rename `token` → `sessionToken`
- [ ] Add test for `null` payload


<details>
<summary>Reasoning</summary>
Renaming improves clarity across auth services.
</details>

<h3>Suggested Changes</h3>
<ul>
<li><input type="checkbox"> Rename <code>token</code> → <code>sessionToken</code></li>
<li><input type="checkbox"> Add test for <code>null</code> payload</li>
</ul>


<details>
<summary>Reasoning</summary>
Renaming improves clarity across auth services.
</details>

`#0969DA`

| Endpoint | Expected | Actual |
|------------------|----------|--------|
| POST /session | 200 OK | 200 OK |
| DELETE /session | 204 NoCt | 500 ❌ |

<table>
<tr><th>Endpoint</th><th>Expected</th><th>Actual</th></tr>
<tr><td>POST /session</td><td>200 OK</td><td>200 OK</td></tr>
<tr><td>DELETE /session</td><td>204 NoCt</td><td>500 ❌</td></tr>
</table>

<details>
<summary>Edge Cases</summary>
- Company 1
- Company 2
</details>

- Company 1
- Company 2

<details>
<summary>Edge Cases</summary>
<ul>
<li>Token refresh fails if expired > 12h</li>
<li>Mobile client retries 3×</li>
</ul>
</details>

> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```
