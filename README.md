# Founder Skills for Claude Code

Two Claude Code skills for founders. Built from real usage across 50+ investor and design partner conversations.

## What's Inside

### `founder-debrief`

Structured post-conversation extraction that turns every investor pitch, customer call, partner meeting, or advisor session into a system update. Instead of scattered notes that decay, you get insights routed to canonical files that compound over time.

**What it does:**
- Walks through an 8-section extraction template (what resonated, what confused them, pushback, unanswered questions, positioning drift, next steps, positioning changes, proof gaps)
- Routes each insight to the right canonical file with persona tags
- Maintains a canonical file system: talk tracks, objections, discovery, decisions, current state, and relationships
- Quality checks for verbatim phrases, concrete next steps, and source attribution

**Trigger phrases:** "debrief", "conversation extraction", "what resonated", "meeting notes", "post-meeting review"

### `neurodivergent-founder`

ADHD and neurodivergent-aware interaction rules for founders using Claude Code as a business operating system. Changes how Claude communicates, creates tasks, structures outreach, and runs daily routines.

**What it does:**
- Enforces 7 behavioral rules: no shame/pressure, RSD accommodation, effort over outcomes, gradual ramps, choices not commands, freeze response handling, energy-aware task design
- Implements energy mode framework (Quick Win / Deep Focus / People / Admin) for context-batched task management
- Provides outreach patterns that respect rejection sensitivity
- Includes a drop-in CLAUDE.md section for permanent behavioral rules

**Trigger phrases:** "ADHD", "neurodivergent", "energy modes", "executive function", "task batching"

## Installation

### Option 1: Copy to your skills directory

```bash
# Clone the repo
git clone https://github.com/assafkipnis/founder-skills.git

# Copy skills to your Claude Code skills directory
cp -r founder-skills/skills/* ~/.claude/skills/
```

### Option 2: Symlink (recommended for staying up to date)

```bash
git clone https://github.com/assafkipnis/founder-skills.git ~/founder-skills

# Symlink each skill
ln -s ~/founder-skills/skills/founder-debrief ~/.claude/skills/founder-debrief
ln -s ~/founder-skills/skills/neurodivergent-founder ~/.claude/skills/neurodivergent-founder
```

### Option 3: Git submodule (for project-specific installation)

```bash
# From your project root
git submodule add https://github.com/assafkipnis/founder-skills.git .claude/founder-skills

# Symlink skills
ln -s .claude/founder-skills/skills/founder-debrief .claude/skills/founder-debrief
ln -s .claude/founder-skills/skills/neurodivergent-founder .claude/skills/neurodivergent-founder
```

### Verify installation

After installing, start a Claude Code session and ask Claude to debrief a conversation or mention ADHD/energy modes. The skills should activate automatically based on trigger phrases.

## Why These Exist

The Claude Code skills ecosystem (380+ skills) is almost entirely developer-focused - linting, testing, deployment, code review. Nothing exists for the operational side of running a company: extracting insights from conversations, managing neurodivergent workflows, or building a compounding knowledge system from founder interactions.

These skills fill that gap. They were built by a founder with ADHD running a pre-seed startup entirely through Claude Code, and refined across months of daily use.

## Using Them Together

The two skills are designed to work together:

1. After a conversation, invoke `founder-debrief` to extract and route insights
2. Follow-up tasks from the debrief automatically get energy tags and time estimates (from `neurodivergent-founder`)
3. Daily routines surface debrief follow-ups organized by energy mode
4. Outreach suggested by debriefs follows the gradual ramp pattern

You can also use each skill independently.

## Credits

- [ravila4/claude-adhd-skills](https://github.com/ravila4/claude-adhd-skills) - Complementary ADHD skills focused on developer time management, Pomodoro tracking, and Obsidian journaling. Use alongside `neurodivergent-founder` for full coverage.
- [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) - Marketing skills for Claude Code that inspired the skill packaging pattern.

## License

MIT. See [LICENSE](LICENSE).
