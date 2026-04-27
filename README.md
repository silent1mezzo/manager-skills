# manager-skills

Claude Code skills for Engineering Managers. These slash commands help you stay on top of your team and your day without manually digging through Linear, GitHub, Slack, and your calendar.

## Skills

### `/brain`

Generates a team status snapshot by searching Linear and GitHub. Run this when you want a quick read on what everyone is working on before standup or a planning session.

**What it produces:**
- Per-engineer summary: current project/initiative, how long they've been on their latest tickets, and what's up next
- Flags for concerns: very large PRs, reduced velocity, tickets open longer than a week
- A list of items worth raising in standup

**Team setup:** The skill reads your team roster from `TEAM.md` in the working directory. If the file doesn't exist, it will ask you to provide your team and create it.

**Usage:**
```
/brain
```

---

### `/good-morning`

Runs a full morning briefing. Use this at the start of your day to orient yourself before diving into work.

**What it produces:**
- Summary of all meetings for the day
- Prep doc for each meeting (agenda, context, open questions)
- For 1:1s: pulls the relevant Notion page from your personal 1:1s section to surface prior notes
- Strategic focus doc with your top 3 priorities for the day
- Team status snapshot (runs `/brain` automatically)

**Usage:**
```
/good-morning
```

---

## Setup

### Prerequisites

These skills rely on the following integrations being connected in Claude Code:

| Integration | Used by |
|---|---|
| Linear | `/brain`, `/good-morning` |
| GitHub (`gh`) | `/brain`, `/good-morning` |
| Slack | `/good-morning` |
| Google Calendar | `/good-morning` |
| Notion | `/good-morning` |

### TEAM.md

Create a `TEAM.md` file in this directory listing your direct reports. If it's missing, `/brain` will prompt you to add it. Example format:

```markdown
# Team

- Alice Smith (alice@example.com)
- Bob Jones (bob@example.com)
- Carol Lee (carol@example.com)
```

### Installing the skills

Clone this repo and run `claude` from within it — no installation or symlinking needed.

```
git clone <repo-url>
cd manager-skills
claude
```
