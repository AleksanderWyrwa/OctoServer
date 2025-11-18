# GitHub-Flavored Markdown + HTML Workshop (Caseform)

# Why Markdown + HTML?

  * Structured PR comments
  * Clear GitHub Discussionsz
  * Enhanced READMEs and documentation

> Tip: Good formatting reduces reviewer fatigue. ✅

---

# PR Review Examples

### Markdown Example

```markdown
### Suggested Changes
- [ ] Rename `token` → `sessionToken` /* clearer meaning */
- [ ] Add null-payload test /* covers mobile client edge case */

<details>
<summary>Reasoning</summary>
The naming aligns with our auth service conventions.
</details>
```

**Rendered Result:**

### Suggested Changes

* [ ] Rename `token` → `sessionToken` /* clearer meaning */
* [ ] Add null-payload test /* covers mobile client edge case */

<details>
<summary>Reasoning</summary>
The naming aligns with our auth service conventions.
</details>

---

# Tables

### Markdown Table

```markdown
| Endpoint        | Expected | Actual |
|-----------------|----------|--------|
| POST /session   | 200 OK   | 200 OK |
| DELETE /session | 204 OK   | 500 ❌ |
```

**Rendered Result:**

| Endpoint        | Expected | Actual |
| --------------- | -------- | ------ |
| POST /session   | 200 OK   | 200 OK |
| DELETE /session | 204 OK   | 500 ❌  |

### HTML Table

```html
<table>
  <tr><th>Endpoint</th><th>Expected</th><th>Actual</th></tr>
  <tr><td>POST /session</td><td>200 OK</td><td>200 OK</td></tr>
  <tr><td>DELETE /session</td><td>204 OK</td><td>500 ❌</td></tr>
</table>
```

**Rendered Result:**

<table>
  <tr><th>Endpoint</th><th>Expected</th><th>Actual</th></tr>
  <tr><td>POST /session</td><td>200 OK</td><td>200 OK</td></tr>
  <tr><td>DELETE /session</td><td>204 OK</td><td>500 ❌</td></tr>
</table>

---

# Collapsibles & Spoilers

```markdown
<details>
  <summary>Edge Cases</summary>
  - Token expired > 12h
  - Mobile retries 3×
</details>
```

**Rendered Result:**

<details>
<summary>Edge Cases</summary>
- Token expired > 12h
- Mobile retries 3×
</details>

---

# Code Blocks & Inline Comments

```javascript
// Example Caseform logic
if (!sessionToken) {
  throw new Error("missing session token"); /* reject unauthorized */
}
```

**Rendered Result:**

// Example Caseform logic
if (!sessionToken) {
throw new Error("missing session token"); /* reject unauthorized */
}

---

## Notes / Info

---

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

---

# GitHub Discussions

```markdown
## Action Items
- [ ] Investigate cold-start latency /* backend lambdas */
- [ ] Document retry strategy /* client SDK */
- [ ] Align error schema /* API consistency */

@alice Can you verify logging behavior?
```

**Rendered Result:**

## Action Items

* [ ] Investigate cold-start latency /* backend lambdas */
* [ ] Document retry strategy /* client SDK */
* [ ] Align error schema /* API consistency */

@alice Can you verify logging behavior?

---

# Mermaid Diagrams
<pre> ```mermaid 
  flowchart TD 
  %% Main workflow 
  A[Linear] --> B[Development] 
  B --> C[Pull Request] 
  C --> D[Review]
  D --> E[Merge]
  E --> F[Deploy]
  %% Backflow from Review 
  D -->|Changes Requested| C 
  C -->|Needs Rework| B 
 ``` </pre>

**Rendered Result:**
```mermaid
flowchart TD

    %% Main workflow
    A[Linear] --> B[Development]
    B --> C[Pull Request]
    C --> D[Review]
    D --> E[Merge]
    E --> F[Deploy]

    %% Backflow from Review
    D -->|Changes Requested| C
    C -->|Needs Rework| B
```

---

# Footnotes

```markdown
Some flows rely on OAuth2[^1].

[^1]: https://oauth.net/2/
```

**Rendered Result:**

Some flows rely on OAuth2[^1].

[^1]: [https://oauth.net/2/](https://oauth.net/2/)

---

# Task Lists

```markdown
- [ ] Investigate performance
- [x] Update README
- [ ] Review PR
```

**Rendered Result:**

* [ ] Investigate performance
* [x] Update README
* [ ] Review PR

---

# Blockquotes & Emojis

```markdown
> Remember: clarity is key! 🚀
```

**Rendered Result:**

> Remember: clarity is key! 🚀

---

# Live Workshop Section

* Enhance a Caseform PR review using Markdown + HTML
* Improve a GitHub Discussion
* Update a README section
* Apply task lists, tables, collapsibles, footnotes, and Mermaid diagrams

---

# Summary

* Markdown = simple, fast
* HTML = powerful, flexible
* Combining both → best results in GitHub
* Fully supports Caseform workflow



# Onboarding / Role Update Checklist for New Experienced Developer

### GitHub Teams
- Add them to **Caseform** team
- Remove them from **Caseform (non-reviewers)** team

### TMetric
- Add them as **Team Lead** in **Caseform (Experienced)** team

### Quick Reference / Initials
- Update **Quick Reference** page: move/add their initials

### Slack
- Add them to **@caseform-experienced** user group

### Refinement / Meetings
- Create **Refinement in Progress** section for them
- Update **Controlling spreadsheet**:
  - Set them as next **Refinement Speaker**
  - Add them to **SSE rotation** (re-randomize twice)

### Documentation
- Send them the link to [What are my duties, rights, and responsibilities as experienced developer and refinement speaker?](https://github.com/Caseform/repo/issues/1215)  
      Ask them to read it at their earliest convenience

# frozen_string_literal: true

# 🖌 Caseform Allowed HTML Elements Examples

This file demonstrates all **valid HTML tags** allowed by `SanitizationFilter`.  
Each example is safe to render in GitHub Markdown.

---

## 1️⃣ Headings

<h1>H1 Heading</h1>
<h2>H2 Heading</h2>
<h3>H3 Heading</h3>
<h4>H4 Heading</h4>
<h5>H5 Heading</h5>
<h6>H6 Heading</h6>

---

## 2️⃣ Text Formatting

<p>
<b>Bold</b>, <strong>Strong</strong><br>
<i>Italic</i>, <em>Emphasis</em><br>
<tt>Teletype</tt>, <code>Inline code</code><br>
<del>Deleted</del>, <ins>Inserted</ins><br>
<sub>Subscript</sub>, <sup>Superscript</sup><br>
<s>Strikethrough</s>, <strike>Strike</strike>
</p>

---

## 3️⃣ Links & Media

<a href="https://example.com">Example Link</a><br>
<img src="https://via.placeholder.com/100" alt="Placeholder Image" loading="lazy"><br>

<picture>
  <source srcset="https://via.placeholder.com/100" type="image/png">
  <img src="https://via.placeholder.com/100" alt="Picture Fallback">
</picture>

---

## 4️⃣ Lists

### Ordered List
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ol>

### Unordered List
<ul>
  <li>Apple</li>
  <li>Banana</li>
  <li>Cherry</li>
</ul>

---

## 5️⃣ Tables

<table>
  <thead>
    <tr>
      <th>Element</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>div</td>
      <td>Generic container</td>
    </tr>
    <tr>
      <td>span</td>
      <td>Inline container</td>
    </tr>
    <tr>
      <td>blockquote</td>
      <td>Quoted text</td>
    </tr>
  </tbody>
</table>

---

## 6️⃣ Interactive / Collapsible

<details>
  <summary>Click to see interactive tags</summary>
  <ul>
    <li><kbd>Keyboard Input</kbd></li>
    <li><q>Inline Quote</q></li>
    <li><var>Variable</var></li>
    <li><samp>Sample Output</samp></li>
    <li><abbr title="Hypertext Markup Language">HTML</abbr></li>
  </ul>
</details>

---

## 7️⃣ Semantic & Miscellaneous

<figure>
  <img src="https://via.placeholder.com/80" alt="Example Figure">
  <figcaption>Figure Caption</figcaption>
</figure>

<hr>

<ruby>
  漢 <rt>kan</rt> <rp>(</rp>漢<rt>kan</rt><rp>)</rp>
</ruby>

<time datetime="2025-11-18">November 18, 2025</time>

---

## 8️⃣ Blockquotes & Emphasis

<blockquote>
  Remember: Clarity is key! 🚀
</blockquote>

---

## 9️⃣ Code Blocks

<pre><code class="language-ruby">
# Ruby example
puts "Hello Caseform!"
</code></pre>

---

## 10️⃣ Challenge Section

> [!TIP]
> Add your own allowed HTML tags here to experiment.  
> Use `<details>`, `<kbd>`, `<blockquote>`, `<table>`, `<img>`, `<figure>`, etc.  

