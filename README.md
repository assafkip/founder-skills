# Founder Skills for Claude Code

You just had an investor call. You remember it went well. You think they pushed back on pricing. You're not sure what you said about competition. The follow-up email is due tomorrow and you don't know what to write.

These two skills fix that.

## What this is

Two Claude Code skills built for founders who run their business through AI. One captures what happens in every conversation so nothing gets lost. The other makes Claude stop talking to you like a productivity app and start working with how your brain actually works.

Built by a founder with ADHD running a pre-seed startup entirely through Claude Code. Refined across 50+ investor and design partner conversations.

## The skills

### `founder-debrief`

Run this after any investor pitch, customer call, or advisor session. It walks you through 8 extraction questions and routes every insight to the right place: what resonated goes to your talk tracks, pushback goes to your objections file, next steps become tasks.

**Without this:** Notes decay in Google Docs. You forget what landed. You repeat mistakes.

**With this:** Every conversation compounds. Your pitch gets sharper automatically.

### `neurodivergent-founder`

Changes how Claude talks to you. No "you need to do this today." No guilt about missed follow-ups. No 12-item urgent lists that trigger a freeze response.

Instead: tasks tagged by energy level (Quick Win / Deep Focus / People / Admin), outreach framed as sharing expertise instead of asking favors, and choices instead of commands.

**Without this:** Claude acts like every other productivity tool that makes you feel behind.

**With this:** Claude works with your brain instead of against it.

## Install

```bash
git clone https://github.com/assafkip/founder-skills.git
cp -r founder-skills/skills/* ~/.claude/skills/
```

<details>
<summary>Other install methods</summary>

**Symlink (stays up to date):**
```bash
git clone https://github.com/assafkip/founder-skills.git ~/founder-skills
ln -s ~/founder-skills/skills/founder-debrief ~/.claude/skills/founder-debrief
ln -s ~/founder-skills/skills/neurodivergent-founder ~/.claude/skills/neurodivergent-founder
```

**Git submodule:**
```bash
git submodule add https://github.com/assafkip/founder-skills.git .claude/founder-skills
ln -s .claude/founder-skills/skills/founder-debrief .claude/skills/founder-debrief
ln -s .claude/founder-skills/skills/neurodivergent-founder .claude/skills/neurodivergent-founder
```
</details>

After installing, just mention "debrief" after a conversation or "ADHD" / "energy modes" in any session. The skills activate automatically.

## Why these exist

The Claude Code skills ecosystem is almost entirely developer-focused. Linting, testing, deployment, code review. Nothing for the operational side of actually running a company.

If you're a founder using Claude Code as your operating system, these are for you.

## Credits

- [ravila4/claude-adhd-skills](https://github.com/ravila4/claude-adhd-skills) - Complementary ADHD skills for developer workflows
- [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) - Marketing skills that inspired the packaging pattern

[MIT License](LICENSE)
