---
name: founder-debrief
description: >
  Structured post-conversation extraction for founders. Invoke when the user says
  "debrief", "conversation extraction", "what resonated", "meeting notes",
  "post-meeting review", or describes a conversation they just had with an investor,
  customer, partner, or advisor and wants to capture what they learned.
metadata:
  version: 1.0.0
  author: Assaf Kipnis
  tags: [founder, debrief, conversation, extraction, positioning, canonical]
---

# Founder Debrief

Extract structured insights from founder conversations (investor pitches, customer discovery, partner meetings, advisor calls) and route them to the right canonical files so nothing gets lost and positioning compounds over time.

Most founders leave conversations with scattered notes or nothing at all. This skill turns every conversation into a system update - capturing exact phrases that resonated, objections that need answers, and positioning drift before it becomes a problem.

## Before Starting

1. Check if the user has a canonical file system set up. Look for files like `canonical/talk-tracks.md`, `canonical/objections.md`, or similar in the project directory.
2. If no canonical files exist, ask: "You don't have canonical files set up yet. Want me to create the starter set? (See `references/canonical-files.md` for what each file does.)"
3. If canonical files exist, read them so you can route new insights correctly and avoid duplicating what's already captured.

## When to Use

- After any conversation with an investor, customer, design partner, advisor, or industry contact
- When the user pastes meeting notes and wants them processed
- When the user describes a conversation from memory
- During batch processing of multiple conversation notes
- Any time the user says "debrief" or asks to extract insights from a conversation

## The 8-Section Extraction Template

For every conversation, extract these 8 sections. If a section has nothing, write "Nothing new" - never skip a section.

### 1. What Resonated (exact phrases)
Capture the specific language, metaphors, or framings that made the other person lean in, nod, or say "that's interesting." Use their exact words when possible.

**Route to:** `canonical/talk-tracks.md` under the relevant persona tag

**Format:**
```
- "[exact phrase or framing]" - got [reaction] from [persona type]
  Context: [what you were discussing when this landed]
```

### 2. What Confused Them
Moments where they asked for clarification, looked lost, or you had to re-explain. These are positioning problems - if one person is confused, others will be too.

**Route to:** `canonical/objections.md` as clarity gaps

**Format:**
```
- Confusion: [what they didn't get]
  Root cause: [why - was it jargon? wrong abstraction level? missing context?]
  Better framing: [if you found one during the conversation]
```

### 3. What They Pushed Back On
Direct disagreements, skepticism, or "yeah, but..." moments. These become objections that need crisp answers.

**Route to:** `canonical/objections.md` under the relevant persona tag

**Format:**
```
- Objection: "[their words]"
  Your response: [what you said]
  Did it land? [yes/no/partially]
  Better answer needed? [yes/no + notes]
```

### 4. What They Asked That You Couldn't Answer
Questions where you stumbled, deflected, or said "good question, let me think about that." These are gaps that need filling before the next similar conversation.

**Route to:** `canonical/discovery.md` as open questions

**Format:**
```
- Question: "[their question]"
  Your response: [what you said, if anything]
  Answer needed by: [next conversation type where this will come up]
```

### 5. Positioning Drift Check
Did they understand what you're building? Did they compare you to the wrong thing? Did they slot you into a category you don't belong in?

**Route to:** `canonical/objections.md` as misclassification risks, `canonical/talk-tracks.md` if you found a correction that worked

**Format:**
```
- They thought we were: [what they compared you to or categorized you as]
  We're actually: [correct positioning]
  Correction that worked: [if you found one]
  Correction needed: [if you didn't]
```

### 6. Next Step Agreed
Concrete next actions with owners and timelines. Not vague "let's stay in touch" - actual commitments.

**Route to:** Task system / CRM / `my-project/relationships.md`

**Format:**
```
- Action: [specific action]
  Owner: [who]
  Timeline: [when]
  Trigger: [what needs to happen first, if anything]
```

### 7. Changes to Positioning
If the conversation revealed that something in your current positioning needs updating - a number that's wrong, a claim that's overclaiming, a framing that doesn't work.

**Route to:** `my-project/current-state.md`, relevant canonical files

**Format:**
```
- Change: [what needs updating]
  Reason: [what the conversation revealed]
  Files affected: [which canonical files need updating]
  Urgency: [before next pitch / this week / when convenient]
```

### 8. Proof Gaps Exposed
Moments where you needed data, a case study, a testimonial, or a reference and didn't have it. These compound - track them so you can fill them systematically.

**Route to:** `canonical/discovery.md` as proof gaps

**Format:**
```
- Proof needed: [what type of evidence]
  Context: [when it came up and why it mattered]
  Potential source: [where you might get this, if known]
```

## Routing Logic Summary

| Insight Type | Primary Destination | Tag With |
|---|---|---|
| Resonant phrases | `canonical/talk-tracks.md` | Persona, date, context |
| Confusions | `canonical/objections.md` | Persona, root cause |
| Pushback/objections | `canonical/objections.md` | Persona, response quality |
| Unanswered questions | `canonical/discovery.md` | Urgency, next occurrence |
| Positioning drift | `canonical/objections.md` + `talk-tracks.md` | Misclassification type |
| Next steps | Task system / `my-project/relationships.md` | Owner, timeline |
| Positioning changes | `my-project/current-state.md` | Urgency, files affected |
| Proof gaps | `canonical/discovery.md` | Evidence type, source |

See `references/routing-map.md` for detailed examples of each routing path.

## Quality Checklist

Before finalizing the debrief, verify:

- [ ] **Verbatim phrases captured** - Did you use their exact words, not paraphrases, for what resonated and what they pushed back on?
- [ ] **Persona tagged** - Is every insight tagged with who said it (VC, customer, partner, advisor, etc.)?
- [ ] **Next steps are concrete** - Do all next steps have an owner, a timeline, and a trigger condition?
- [ ] **Source attributed** - Can you trace every insight back to a specific moment in the conversation?
- [ ] **No overclaiming** - Did you mark anything uncertain with an appropriate flag (e.g., {{NEEDS_VALIDATION}})?
- [ ] **Routing complete** - Has every section been routed to the correct canonical file?
- [ ] **Duplicates checked** - Did you verify these insights don't already exist in the canonical files?

## Workflow

1. **Gather context**: Ask the user who they spoke with, their role, company, and date. Check existing relationship data if available.
2. **Process the conversation**: Walk through the 8 sections. Ask clarifying questions if the user's notes are vague - "When you say they pushed back, what were their exact words?"
3. **Draft the debrief**: Present the full 8-section extraction for review.
4. **Route insights**: After user approval, update each canonical file with the new insights. Show what changed.
5. **Create follow-ups**: Turn next steps into tasks in the user's task system. Tag with energy mode and time estimate if the user uses that framework.
6. **Log the interaction**: Update relationship tracking with conversation date, key takeaways, and next touch point.

## Setup Guide

If you're starting from scratch, see `references/canonical-files.md` for how to create the 6 core canonical files. The minimum viable setup is:

1. `canonical/talk-tracks.md` - Proven language organized by persona
2. `canonical/objections.md` - Objections with answers, organized by persona
3. `canonical/discovery.md` - Open questions and validated answers

You can add the other 3 (`decisions.md`, `my-project/current-state.md`, `my-project/relationships.md`) as your system matures.

## Related Skills

- **neurodivergent-founder** - If the user has ADHD/neurodivergent traits, follow-up tasks from debriefs should use energy modes and time estimates
- **product-marketing-context** - Debrief insights feed directly into marketing positioning
