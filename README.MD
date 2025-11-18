# GitHub-Flavored Markdown + HTML Workshop (Caseform)

Welcome to a full demo of **everything Markdown can do** in the context of Caseform.

---

## Table of Contents

1. [Why Markdown Matters](#why-markdown-matters)
2. [PR Review Examples](#pr-review-examples)
3. [Tables](#tables)
4. [Collapsibles & Spoilers](#collapsibles--spoilers)
5. [Code Blocks and Inline Comments](#code-blocks-and-inline-comments)
6. [GitHub Discussions](#github-discussions)
7. [Mermaid Diagrams](#mermaid-diagrams)
8. [Footnotes](#footnotes)
9. [Task Lists](#task-lists)
10. [Blockquotes & Emojis](#blockquotes--emojis)
11. [Live Workshop Section](#live-workshop-section)

---

## Why Markdown Matters

- Our workflow: **Linear → Dev → PR → Review → Merge**
- Stories already descriptive → PR descriptions optional
- Markdown + HTML improve:
  - PR review comments
  - GitHub Discussions
  - Documentation and READMEs

> Note: Good formatting reduces reviewer fatigue. ✅

---

## PR Review Examples

### Markdown Example

```markdown
### Suggested Changes
- [ ] Rename `token` → `sessionToken` /* clearer meaning */
- [ ] Add null-payload test /* covers mobile client edge case */

<details>
<summary>Reasoning</summary>
The naming aligns with our auth service conventions.
</details>
Rendered Result:

Suggested Changes
 Rename token → sessionToken /* clearer meaning */

 Add null-payload test /* covers mobile client edge case */

<details> <summary>Reasoning</summary> The naming aligns with our auth service conventions. </details>
HTML Example
html
Skopiuj kod
<h3>Suggested Changes</h3>
<ul>
  <li><input type="checkbox"> Rename <code>token</code> → <code>sessionToken</code></li>
  <li><input type="checkbox"> Add null payload test</li>
</ul>
<details>
  <summary>Reasoning</summary>
  Aligns with our service-level naming.
</details>
Rendered Result:

<h3>Suggested Changes</h3> <ul> <li><input type="checkbox"> Rename <code>token</code> → <code>sessionToken</code></li> <li><input type="checkbox"> Add null payload test</li> </ul> <details> <summary>Reasoning</summary> Aligns with our service-level naming. </details>
Tables
Markdown Table
markdown
Skopiuj kod
| Endpoint        | Expected | Actual |
|-----------------|----------|--------|
| POST /session   | 200 OK   | 200 OK |
| DELETE /session | 204 OK   | 500 ❌ |
Rendered Result:

Endpoint	Expected	Actual
POST /session	200 OK	200 OK
DELETE /session	204 OK	500 ❌

HTML Table
html
Skopiuj kod
<table>
  <tr><th>Endpoint</th><th>Expected</th><th>Actual</th></tr>
  <tr><td>POST /session</td><td>200 OK</td><td>200 OK</td></tr>
  <tr><td>DELETE /session</td><td>204 OK</td><td>500 ❌</td></tr>
</table>
Rendered Result:

<table> <tr><th>Endpoint</th><th>Expected</th><th>Actual</th></tr> <tr><td>POST /session</td><td>200 OK</td><td>200 OK</td></tr> <tr><td>DELETE /session</td><td>204 OK</td><td>500 ❌</td></tr> </table>
Collapsibles & Spoilers
markdown
Skopiuj kod
<details>
  <summary>Edge Cases</summary>
  - Token expired > 12h
  - Mobile retries 3×
</details>
Rendered Result:

<details> <summary>Edge Cases</summary> - Token expired > 12h - Mobile retries 3× </details>
Code Blocks and Inline Comments
javascript
Skopiuj kod
// Example Caseform logic
if (!sessionToken) {
  throw new Error("missing session token"); /* reject unauthorized */
}
Rendered Result:

// Example Caseform logic
if (!sessionToken) {
throw new Error("missing session token"); /* reject unauthorized */
}

GitHub Discussions
markdown
Skopiuj kod
## Action Items
- [ ] Investigate cold-start latency /* backend lambdas */
- [ ] Document retry strategy /* client SDK */
- [ ] Align error schema /* API consistency */

@alice Can you verify logging behavior?
Rendered Result:

Action Items
 Investigate cold-start latency /* backend lambdas */

 Document retry strategy /* client SDK */

 Align error schema /* API consistency */

@alice Can you verify logging behavior?

Mermaid Diagrams
mermaid
Skopiuj kod
graph TD
  Linear --> Dev
  Dev --> PR
  PR --> Review
  Review --> Merge
Rendered Result: (Mermaid diagram rendered by GitHub or Mermaid viewer)

Footnotes
markdown
Skopiuj kod
Some flows rely on OAuth2[^1].

[^1]: https://oauth.net/2/
Rendered Result:

Some flows rely on OAuth21.

Task Lists
markdown
Skopiuj kod
- [ ] Investigate performance
- [x] Update README
- [ ] Review PR
Rendered Result:

 Investigate performance

 Update README

 Review PR

Blockquotes & Emojis
markdown
Skopiuj kod
> Remember: clarity is key! 🚀
Rendered Result:

Remember: clarity is key! 🚀

Live Workshop Section
Enhance a real Caseform PR review using Markdown + HTML

Improve one GitHub Discussion

Update a README section

Apply task lists, tables, collapsibles, and footnotes

Summary
Markdown = fast and clean

HTML = flexible and powerful

Combining both gives the best experience for Caseform workflow

Everything is rendered in GitHub or VSCode automatically

pgsql
Skopiuj kod

This is a fully **ready Markdown file**, showcasing all Markdown features with examples and results directly below each snippet.  

I can now create a **version with even more features**, like embedded images, badges, syntax highlighting, and color-coded HTML inside Markdown if you want. Do you want me to do that next?
Footnotes
https://oauth.net/2/ ↩
