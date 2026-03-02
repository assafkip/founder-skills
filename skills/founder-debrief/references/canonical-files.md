# Canonical File System

Canonical files are your single source of truth for positioning, objections, and relationship intelligence. They compound over time - every conversation makes them more valuable.

The key principle: **one fact, one place.** If your competitive positioning lives in both your pitch deck and a random notes file, they will drift apart. Canonical files prevent that.

## Core Files

### 1. `canonical/talk-tracks.md`

**What it holds:** Proven language that works, organized by persona.

**Structure:**

```markdown
# Talk Tracks

## By Persona

### Investors (VC / Angel)
- **One-liner:** "[your tested one-liner for investors]"
- **Problem framing:** "[how you frame the problem for investors]"
- **Differentiator:** "[what makes you different, in investor language]"
- **Proof points:** "[evidence that resonates with investors]"

### Customers ([your customer type])
- **One-liner:** "[your tested one-liner for customers]"
- **Problem framing:** "[how you frame the problem for customers]"
- ...

### Partners
- ...

### Advisors / Industry
- ...

## Tested Phrases
Phrases that consistently land across personas:
- "[phrase]" - works because [why]. First tested [date], confirmed [N] times.
- "[phrase]" - works because [why]. First tested [date], confirmed [N] times.

## Retired Phrases
Phrases that stopped working or were replaced:
- "[phrase]" - replaced by "[new phrase]" on [date]. Reason: [why].
```

**Rules:**
- Only add language here that has been tested in a real conversation and got a positive reaction
- Tag every phrase with the persona it worked with and the date it was first tested
- When a phrase stops working, move it to "Retired" with the reason, don't delete it
- Review monthly for staleness

---

### 2. `canonical/objections.md`

**What it holds:** Every objection you've heard, organized by persona, with your best current answer.

**Structure:**

```markdown
# Objections

## By Persona

### Investor Objections
#### "[Objection in their words]"
- **Frequency:** [how often this comes up: rare / occasional / every pitch]
- **Best answer:** "[your current best response]"
- **What NOT to say:** "[responses that backfired]"
- **Proof needed:** [what evidence would kill this objection]
- **Last updated:** [date]

### Customer Objections
#### "[Objection in their words]"
- ...

### Misclassification Risks
#### "So you're like [wrong comparison]?"
- **Correction:** "[what works to redirect]"
- **Why they think this:** [root cause of the misclassification]
- ...

## Clarity Gaps
Things that confuse people (not objections, but positioning problems):
- **[Topic]:** People get confused because [reason]. Better framing: "[what works]"
```

**Rules:**
- Use their exact words as the objection header, not your paraphrase
- Track frequency - if an objection comes up every pitch, your positioning has a problem
- "What NOT to say" is as valuable as "Best answer" - learn from failures
- Misclassification risks are separate from objections. An objection is "I don't think this works." Misclassification is "I think this is something else."

---

### 3. `canonical/discovery.md`

**What it holds:** Open questions, validated answers, and proof gaps.

**Structure:**

```markdown
# Discovery

## Validated Answers
Questions that have been answered - do not re-ask these:
- **Q:** [question]
  **A:** [validated answer]
  **Source:** [who/what validated this]
  **Date:** [when]

## Open Questions
Questions that still need answers:
- **Q:** [question]
  **Priority:** [high / medium / low]
  **Comes up in:** [which conversation types]
  **Potential sources:** [where to find the answer]

## Proof Gaps
Evidence you need but don't have:
- **Need:** [type of proof]
  **Why:** [what conversation moment needs it]
  **Potential source:** [where to get it]
  **Priority:** [high / medium / low]

## Positioning Decisions
Decisions made about positioning that should not be revisited without good reason:
- **Decision:** [what was decided]
  **Reason:** [why]
  **Date:** [when]
  **Revisit if:** [conditions that would warrant reopening]
```

**Rules:**
- Move questions to "Validated" as soon as they're answered, don't leave them open
- Proof gaps should be reviewed weekly and actively pursued
- Positioning decisions prevent re-litigating settled questions. Respect them.

---

### 4. `canonical/decisions.md`

**What it holds:** Active rules that govern your positioning, messaging, and behavior.

**Structure:**

```markdown
# Decisions

## Active Rules

### RULE-001: [Short name]
- **Rule:** [what the rule requires or prohibits]
- **Reason:** [why this rule exists]
- **Date:** [when decided]
- **Example:** [what following this rule looks like]
- **Violation example:** [what breaking this rule looks like]

### RULE-002: [Short name]
- ...
```

**Rules:**
- Number rules sequentially for easy reference
- Every rule needs a "Reason" - rules without reasons get ignored
- Include both positive and negative examples
- Review quarterly. Rules that no longer apply should be marked as retired, not deleted.
- Keep the count manageable. More than 20 active rules suggests some should be consolidated.

---

### 5. `my-project/current-state.md`

**What it holds:** What is true about your company RIGHT NOW. Updated after every significant change.

**Structure:**

```markdown
# Current State

**Last updated:** [date]

## Product
- Stage: [idea / prototype / MVP / beta / GA]
- What's built: [honest assessment]
- What's planned: [roadmap items, marked as not built]
- Key metrics: [if any]

## Fundraising
- Stage: [pre-seed / seed / series A / bootstrapped]
- Status: [actively raising / not raising / closing]
- Key relationships: [active investor conversations]

## Team
- [who's on board and their roles]

## Traction
- [customers, pilots, LOIs, conversations - be honest about what each is]

## What's Changed Recently
- [date]: [change and why]
- [date]: [change and why]
```

**Rules:**
- Honesty is mandatory. If you only have conversations, don't call them partnerships.
- Mark anything unvalidated. {{UNVALIDATED}} for claims you haven't proven. {{PLANNED}} for things not built yet.
- Update the "What's Changed" section after every debrief that reveals a state change
- This file feeds your pitch deck. If this file is wrong, your deck is wrong.

---

### 6. `my-project/relationships.md`

**What it holds:** Key contacts, conversation history, and relationship status.

**Structure:**

```markdown
# Relationships

## [Person Name]
- **Role:** [their title and company]
- **Type:** [VC / Customer / Partner / Advisor / Connector / Other]
- **Status:** [active / warm / cold / stalled]
- **First contact:** [date]
- **Last contact:** [date]
- **Key context:** [what matters about this relationship]
- **Conversation log:**
  - [date]: [brief summary + link to debrief if exists]
- **Next step:** [what's pending]
- **Notes:** [anything else relevant]
```

**Rules:**
- Update after every conversation (the debrief workflow does this automatically)
- "Status" should be honest. If someone hasn't responded in 2+ weeks, they're cold.
- "Key context" should include what they care about so you can personalize follow-ups
- Don't track everyone. Focus on relationships that matter to your current stage.

---

## Getting Started

**Minimum viable setup (3 files):**
1. Create `canonical/talk-tracks.md` - Start with your current best pitch language
2. Create `canonical/objections.md` - Start with objections you've already heard
3. Create `canonical/discovery.md` - Start with your open questions

**Full setup (6 files):**
Add `canonical/decisions.md`, `my-project/current-state.md`, and `my-project/relationships.md`.

**Directory structure:**
```
your-project/
  canonical/
    talk-tracks.md
    objections.md
    discovery.md
    decisions.md
  my-project/
    current-state.md
    relationships.md
```

The `canonical/` directory holds positioning truth that applies across all conversations. The `my-project/` directory holds project-specific state. This separation matters when your positioning is stable but your project state changes frequently (e.g., during fundraising).
