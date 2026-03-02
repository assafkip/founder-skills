# Routing Map

How insights from debriefs flow into canonical files. Each example shows a real-world extraction pattern.

## Routing Table

| Debrief Section | Destination File | What Gets Added | Persona Tag |
|---|---|---|---|
| What Resonated | `canonical/talk-tracks.md` | Tested phrase + reaction + context | Required |
| What Confused | `canonical/objections.md` (Clarity Gaps) | Confusion point + root cause + better framing | Required |
| Pushback | `canonical/objections.md` (By Persona) | Objection + response + effectiveness | Required |
| Unanswered Questions | `canonical/discovery.md` (Open Questions) | Question + priority + next occurrence | Optional |
| Positioning Drift | `canonical/objections.md` (Misclassification) + `talk-tracks.md` | Wrong category + correction phrase | Required |
| Next Steps | Task system + `my-project/relationships.md` | Action + owner + timeline | N/A |
| Positioning Changes | `my-project/current-state.md` + affected canonical files | What changed + why + urgency | N/A |
| Proof Gaps | `canonical/discovery.md` (Proof Gaps) | Evidence needed + context + source | Optional |

## Routing Examples

### Example 1: Investor Pitch Debrief

**Conversation:** 30-minute pitch to a Series A VC.

**Section 1 - What Resonated:**
> Debrief says: "When I said 'every team has 60 tools but no coordination layer,' the partner said 'that's exactly what we see in our portfolio companies.'"

**Routes to** `canonical/talk-tracks.md`:
```markdown
### Investors (VC)
- **Problem framing:** "Every team has 60 tools but no coordination layer"
  - Reaction: Partner confirmed pattern across portfolio
  - First tested: 2026-01-15, confirmed 3 times
```

---

**Section 3 - Pushback:**
> Debrief says: "They asked 'Why can't the existing vendors just add this?' I said existing tools are optimized for execution, not coordination. They seemed partially convinced."

**Routes to** `canonical/objections.md`:
```markdown
### Investor Objections
#### "Why can't [incumbent] just add this?"
- **Frequency:** every pitch
- **Best answer:** "Existing tools are optimized for [what they do well], not [your category]. Adding [your capability] would require rearchitecting their core product."
- **What NOT to say:** Don't trash the incumbents. Investors may have them in portfolio.
- **Did it land?** Partially. Need a crisper version.
- **Last updated:** 2026-01-15
```

---

**Section 5 - Positioning Drift:**
> Debrief says: "They kept calling us 'an automation tool.' We're a governance layer."

**Routes to** `canonical/objections.md` (Misclassification):
```markdown
### Misclassification Risks
#### "So you're an automation tool?"
- **Correction:** "Automation tools execute tasks. We govern the process those tasks fit into - who owns what, what's approved, what's the provenance."
- **Why they think this:** The word 'workflow' triggers 'automation' for most VCs.
```

---

### Example 2: Customer Discovery Call

**Conversation:** 45-minute call with a VP of Engineering at a Series B startup.

**Section 2 - What Confused:**
> Debrief says: "When I described the pipeline concept, they asked 'so is this like CI/CD for [my domain]?' I had to backtrack and explain it's not about deployment."

**Routes to** `canonical/objections.md` (Clarity Gaps):
```markdown
## Clarity Gaps
- **Pipeline concept:** Technical buyers default to CI/CD analogy. Better framing: "Think of it as a review and approval workflow, not a deployment pipeline. Every artifact gets reviewed, approved, and tracked - like a change management process, not a build system."
```

---

**Section 4 - Unanswered:**
> Debrief says: "They asked 'How does this handle conflicting inputs from different teams?' I said we'd handle it through governance rules but didn't have a concrete example."

**Routes to** `canonical/discovery.md`:
```markdown
## Open Questions
- **Q:** How do you handle conflicting inputs from different teams?
  **Priority:** high
  **Comes up in:** customer discovery (technical buyers)
  **Potential sources:** Talk to existing design partners about their conflict resolution process
```

---

### Example 3: Advisor Check-in

**Conversation:** 20-minute call with an industry advisor.

**Section 7 - Positioning Changes:**
> Debrief says: "Advisor pointed out that our TAM slide uses a market size from 2023. The 2025 number is 40% higher and there's a Gartner report we should cite."

**Routes to** `my-project/current-state.md`:
```markdown
## What's Changed Recently
- 2026-01-20: TAM number outdated. Need to update from 2023 to 2025 data.
  Source: Gartner report (advisor will send link). Affects pitch deck slide 5.
  Urgency: Before next pitch.
```

Also creates a task:
```
- Action: Update TAM slide with 2025 Gartner data
  Owner: me
  Timeline: Before next pitch (this week)
  Trigger: Advisor sends Gartner link
```

---

**Section 8 - Proof Gaps:**
> Debrief says: "When I mentioned cost savings, they asked 'do you have any data on that?' I didn't."

**Routes to** `canonical/discovery.md`:
```markdown
## Proof Gaps
- **Need:** Cost savings data or benchmark
  **Why:** Advisor asked for evidence during ROI discussion. This will come up with every customer.
  **Potential source:** Design partner pilot data, or industry benchmark from analyst report
  **Priority:** high
```

## Conflict Resolution

When a debrief insight contradicts something already in a canonical file:

1. **Check the source.** Is the existing entry from a more authoritative source?
2. **Check the frequency.** Is the new insight a one-off or does it match a pattern?
3. **When in doubt, keep both.** Add the new insight with a note that it conflicts with the existing entry. Let the founder decide during the next review.
4. **Never silently overwrite.** Always flag conflicts to the user.

## Batch Processing

When processing multiple debriefs at once:

1. Process them chronologically (oldest first)
2. Later conversations may supersede earlier ones - that's fine
3. After all debriefs are processed, do a single dedup pass on each canonical file
4. Flag any contradictions between conversations for the founder to resolve
