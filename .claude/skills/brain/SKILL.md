---
name: brain
description: Searches across Linear, Github, Notion and Slack to understand what a person is working on
allowed-tools: Linear Github(gh *) 
---

You're an Engineering Manager and want to have a better understanding of what your team is currently working on.

Search across Linear and Github PRs (recently opened and cloesd) and craft a summary of the following:

1. The project/intiiative the engineer is working on
2. How long they've been focused on their most recent tickets
3. The next thing they're focused on

Pull the list of teammates from TEAM.md. If this file doesn't exist, ask for their team and add it to TEAM.md

I want you to highlight any concerns (very large PRs, reduced velocity, stuck on a ticket for over a week, etc...)

I'd also like a list of things that should be brought up in standup

For any Linear ticket or GH pr include the URL
