# Research Prompt: AI Startup Idea Finder

Follow every step in order. Steps marked **→ WAIT** require user input before continuing.

---

## STEP 1 — Ask for the broad direction

Say:
> **"What space do you want to explore?"**
> (e.g. healthcare, legal tech, fintech, e-commerce ops, creator economy, construction, remote work, education — or describe the type of problem you're drawn to.)

**→ WAIT for user reply before proceeding.**

---

## STEP 2 — Research & score sub-niches

Run 4–5 searches on the broad niche:
```
[niche] problems Reddit 2025 2026 pain points
[niche] startup opportunities underserved market AI
[niche] "no good tool" OR "manually" OR "takes hours" small business
[niche] micro SaaS opportunity niche 2026
[niche] pain points founder freelancer SMB
```

From the results, identify **5–8 distinct sub-niches**. For each, assess 4 signal dimensions and present them in this format:

---
**[Sub-niche name]**
Market signal: 🔥🔥🔥🔥 · AI leverage: 🤖🤖🤖🤖 · Competition: 🏁 Low · VC interest: 💰💰
*One-sentence description of the core pain and who has it.*

---

**Signal rating guide:**
- 🔥 Market signal (1–4 fires): how frequently this pain appears online — 1 = occasional mentions, 4 = constant complaints across many communities
- 🤖 AI leverage (1–4 robots): how much AI changes the solution — 1 = marginal, 4 = AI is the core unlock that makes this 10x better
- 🏁 Competition: Low / Medium / High — based on number and quality of existing tools
- 💰 VC interest (1–3 coins): how much VC funding has flowed into this space — 1 = minimal, 2 = some early-stage deals, 3 = active funding with recent rounds. High VC interest validates the market but also signals more competition ahead.

Present all sub-niches, then ask:
> "Which one do you want to drill into? Or say **'pick the best one'** and I'll choose the highest-signal sub-niche."

**→ WAIT for user reply before proceeding.**

---

## STEP 2B — Micro-niche drill

Run 2–3 searches to map the specific customer types within the chosen sub-niche:
```
[sub-niche] specific customer types segments
[sub-niche] who uses Reddit community forum discussion
[sub-niche] niche vertical "specifically for"
```

Identify **3–5 micro-niches** — distinct customer types with meaningfully different pain profiles. Present them clearly:

> **Within [sub-niche], I found these specific customer types:**
> 1. **[Micro-niche A]** — e.g. "Mental health therapists (HIPAA + insurance billing specific)"
> 2. **[Micro-niche B]** — e.g. "Life & business coaches (no insurance, different admin pain)"
> 3. **[Micro-niche C]** — ...
>
> Which customer type resonates most? Or should I research across all of them?

**→ WAIT for user reply before proceeding.**

---

## STEP 2C — Niche viability check

Before going deep on research, validate the chosen micro-niche. Run 3 targeted searches:
```
[micro-niche] existing software tools competitors pricing 2025 2026
[micro-niche] market size number of businesses revenue opportunity
[micro-niche] startup funding raised VC investment Crunchbase YCombinator a16z 2022 2023 2024 2025
```

Present a brief **Niche Viability Summary**:

> **Competitive landscape:** [2–3 sentences: who plays here, at what price point, how complete their solutions are]
>
> **Market size signal:** [rough estimate — e.g. "~180,000 licensed solo therapists in the US, most paying $80–200/mo across 3–4 fragmented tools"]
>
> **VC funding landscape:** [List notable companies that raised funding in this niche. For each: company name, amount raised, year, and stage if known. Then interpret: Does VC interest validate the market? Are rounds early-stage (opportunity still open) or late-stage (likely consolidating)? Example: "Clio raised $900M (legal practice mgmt) — validates the market but targets large firms, leaving solo/small firms underserved."]
>
> **Verdict:** 🟢 Green / 🟡 Yellow / 🔴 Red
> - 🟢 Green = clear gap, proceed
> - 🟡 Yellow = crowded but beatable, flag the angle needed to win, ask if user wants to proceed or pivot
> - 🔴 Red = dominated market, strongly recommend pivoting to an adjacent micro-niche

If 🟡 or 🔴, suggest 1–2 adjacent micro-niches to consider before committing.

**Only proceed to Step 3 if user confirms (explicitly or implicitly by not objecting).**

---

## STEP 3 — Deep problem research

Run **6–8 targeted searches** on the confirmed micro-niche:
```
reddit [micro-niche] pain points tool missing frustrated
[micro-niche] "I wish" OR "why is there no" OR "manually" software
[micro-niche] problems no good solution 2025 2026
reddit [micro-niche] "takes hours" OR "waste time" OR "so annoying"
[micro-niche] workflow frustrations Reddit forum community
[micro-niche] SaaS opportunity underserved
```

For each result, extract:
- The specific problem (one sentence)
- Who has it (role / company type / size)
- Frequency signal (rare / common / ubiquitous)
- Whether AI meaningfully solves it

Aim for **15–25 distinct problems**. Duplicate signals across sources = stronger signal, note them.

---

## STEP 4 — Cluster into targeted startup ideas

Group raw problems into **8–12 specific startup ideas**. Each idea must be:
- **Narrow enough** to build an MVP in 6 weeks
- **Named like a product**, not a category (e.g. "AI intake form + insurance verifier for solo therapists" not "healthcare admin tool")
- Solving **one clearly-articulated problem**, not a vague space

---

## STEP 5 — Score each idea

Score 1–5 on each dimension from `reference/idea-evaluation-criteria.md`:

| Dimension | What it measures |
|-----------|-----------------|
| Problem Frequency | How often this appears across sources |
| AI Leverage | Does AI provide a 10x solution? |
| Market Size | How many potential customers? |
| Solution Gap | How bad are current alternatives? |
| Monetization Clarity | Clear, willing buyer? |

Max: 25. Include a one-sentence rationale per score.

---

## STEP 6 — Generate HTML report

Save output as:
```
outputs/YYYY-MM-DD-[niche-slug]-[subniche-slug].html
```

Use this HTML template (replace all `{{placeholders}}`):

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>{{Niche}} — {{Sub-niche}} — {{Date}}</title>
  <style>
    *{box-sizing:border-box;margin:0;padding:0}
    body{font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,sans-serif;background:#0f0f13;color:#e2e2e8;line-height:1.7;padding:40px 20px 80px}
    .container{max-width:900px;margin:0 auto}
    header{border-bottom:1px solid #2a2a36;padding-bottom:28px;margin-bottom:40px}
    h1{font-size:1.8rem;font-weight:700;color:#fff}
    h1 span{color:#7c6cf8}
    .meta{display:flex;gap:10px;margin-top:14px;flex-wrap:wrap}
    .chip{background:#1a1a24;border:1px solid #2a2a36;border-radius:20px;padding:4px 12px;font-size:0.75rem;color:#aaa}
    h2{font-size:1.1rem;font-weight:600;color:#fff;margin:44px 0 16px;padding-bottom:8px;border-bottom:1px solid #1e1e2a}
    table{width:100%;border-collapse:collapse;font-size:0.84rem}
    th{text-align:left;padding:10px 12px;font-size:0.67rem;text-transform:uppercase;letter-spacing:1px;color:#555;background:#1a1a24;white-space:nowrap}
    td{padding:12px;border-bottom:1px solid #1a1a24;vertical-align:top}
    tr:hover td{background:#13131c}
    .rank{color:#555;font-weight:700;text-align:center;width:32px}
    .idea-name{font-weight:600;color:#c4b5fd}
    .problem{color:#aaa}
    .ai{color:#86efac}
    .score-cell{font-weight:700;text-align:right;white-space:nowrap;padding-right:16px}
    .hi{color:#a78bfa}.mid{color:#7dd3fc}.lo{color:#6b7280}
    .bar{display:flex;align-items:center;gap:6px;margin-top:4px}
    .bar-track{height:3px;background:#1e1e2a;border-radius:2px;flex:1}
    .bar-fill{height:100%;border-radius:2px;background:linear-gradient(90deg,#7c6cf8,#a78bfa)}
    .card{background:#13131c;border:1px solid #1e1e2a;border-radius:10px;padding:24px 28px;margin-bottom:20px}
    .card-header{display:flex;align-items:center;gap:12px;margin-bottom:20px}
    .badge{width:32px;height:32px;border-radius:50%;background:linear-gradient(135deg,#7c6cf8,#a78bfa);display:flex;align-items:center;justify-content:center;font-weight:700;font-size:0.85rem;color:#fff;flex-shrink:0}
    .card-title{font-size:1rem;font-weight:700;color:#fff;flex:1}
    .card-score{font-weight:700;color:#a78bfa;font-size:1rem}
    .lbl{font-size:0.67rem;text-transform:uppercase;letter-spacing:1px;color:#7c6cf8;margin-bottom:4px;margin-top:16px}
    .card p{color:#bbb;font-size:0.875rem}
    .scoring-row{display:flex;gap:8px;flex-wrap:wrap;margin-top:6px}
    .score-pill{background:#1a1a24;border:1px solid #2a2a36;border-radius:6px;padding:3px 10px;font-size:0.75rem;color:#aaa}
    .score-pill span{color:#a78bfa;font-weight:600}
    .sources{margin-top:48px}
    .sources ul{list-style:none}
    .sources li{margin-top:8px}
    .sources a{color:#7c6cf8;text-decoration:none;font-size:0.85rem}
    .sources a:hover{text-decoration:underline}
    .viability{background:#13131c;border:1px solid #1e1e2a;border-radius:10px;padding:20px 24px;margin-bottom:32px}
    .viability h3{font-size:0.85rem;font-weight:600;color:#fff;margin-bottom:12px}
    .viability p{color:#aaa;font-size:0.85rem;margin-top:6px}
    .verdict{display:inline-block;padding:2px 10px;border-radius:12px;font-size:0.75rem;font-weight:600;margin-top:10px}
    .green{background:#14532d;color:#86efac}.yellow{background:#713f12;color:#fde68a}.red{background:#7f1d1d;color:#fca5a5}
  </style>
</head>
<body>
<div class="container">
  <header>
    <h1>{{Niche}} — <span>{{Micro-niche}}</span></h1>
    <div class="meta">
      <span class="chip">{{Date}}</span>
      <span class="chip">{{N}} ideas ranked</span>
      <span class="chip">{{signal_count}} signals collected</span>
    </div>
  </header>

  <div class="viability">
    <h3>Niche Viability</h3>
    <p><strong>Competitive landscape:</strong> {{competition_summary}}</p>
    <p><strong>Market size:</strong> {{market_size}}</p>
    <p><strong>VC funding:</strong> {{vc_funding_summary}}</p>
    <span class="verdict {{green|yellow|red}}">{{verdict}}</span>
  </div>

  <h2>Ranked Ideas</h2>
  <table>
    <thead>
      <tr><th>#</th><th>Idea</th><th>Core Problem</th><th>AI Angle</th><th>Score</th></tr>
    </thead>
    <tbody>
      <!-- For each idea: -->
      <tr>
        <td class="rank">{{rank}}</td>
        <td><span class="idea-name">{{idea_name}}</span></td>
        <td class="problem">{{core_problem}}</td>
        <td class="ai">{{ai_angle}}</td>
        <td class="score-cell {{hi|mid|lo}}">{{score}}/25<div class="bar"><div class="bar-track"><div class="bar-fill" style="width:{{pct}}%"></div></div></div></td>
      </tr>
    </tbody>
  </table>

  <h2>Top 3 Deep Dives</h2>
  <!-- Repeat for top 3: -->
  <div class="card">
    <div class="card-header">
      <div class="badge">{{rank}}</div>
      <div class="card-title">{{idea_name}}</div>
      <div class="card-score">{{score}}/25</div>
    </div>
    <div class="lbl">Why the problem is real</div>
    <p>{{why_real}}</p>
    <div class="lbl">Who the customer is</div>
    <p>{{customer}}</p>
    <div class="lbl">How AI makes it 10x better</div>
    <p>{{ai_leverage}}</p>
    <div class="lbl">What a v1 looks like</div>
    <p>{{v1}}</p>
    <div class="lbl">Scoring breakdown</div>
    <div class="scoring-row">
      <span class="score-pill">Frequency <span>{{f}}/5</span></span>
      <span class="score-pill">AI Leverage <span>{{a}}/5</span></span>
      <span class="score-pill">Market <span>{{m}}/5</span></span>
      <span class="score-pill">Solution gap <span>{{g}}/5</span></span>
      <span class="score-pill">Monetization <span>{{mo}}/5</span></span>
    </div>
  </div>

  <h2>Sources</h2>
  <div class="sources">
    <ul><!-- list source links --></ul>
  </div>
</div>
</body>
</html>
```

---

## STEP 7 — Final reply

After saving the HTML file, tell the user:
- The file path of the saved report
- A 2-line summary of the #1 idea
- Offer: drill deeper into any single idea, explore a different micro-niche, or pivot to a new sub-niche
