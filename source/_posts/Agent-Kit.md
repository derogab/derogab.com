---
title: "Agent Kit: my collection of skills and plugins for agents"
date: 2026-02-21 21:21:23
tags:
  - ai
  - agents
  - productivity
  - plugins
  - skills
---

## Introduction

I have always liked tools that save time on repetitive tasks — ever since they were just called “scripts”.

Recently I started spending more time building and testing skills for code agents, so I opened a small repository called [agent-kit](https://github.com/derogab/agent-kit) to collect the ones I find useful in daily work.

It is still early, but it already helps me skip a lot of boring manual steps.

## Why I made it

When working with code agents, I noticed that the same actions come up over and over:
- writing a clean commit message
- preparing a pull request description
- asking for a code review

Each one takes only a moment, but they happen many times a day.
So I decided to package them into reusable skills and plugins.

## What\'s inside

At the moment, [agent-kit](https://github.com/derogab/agent-kit) includes:

[**Skills**](https://skills.sh/derogab/agent-kit) (work with any agent that supports [skills.sh](https://skills.sh)):
- [/commit](https://skills.sh/derogab/agent-kit/commit) — create conventional commits from staged changes
- [/pr](https://skills.sh/derogab/agent-kit/pr) — create or update pull requests with a consistent structure

**Claude Code plugins**:
- **git** — the same /commit and /pr workflow, packaged as a Claude Code plugin
- **sounds** — play sound notifications when the agent needs your attention

The goal is not to be big, but to be practical.

## How to install

### Skills (any compatible agent)

Install the whole set globally:

```bash
npx skills add -g derogab/agent-kit
```

Or pick only what you need:

```bash
npx skills add -g -y derogab/agent-kit@commit
npx skills add -g -y derogab/agent-kit@pr
```

### Claude Code plugins

First, add the marketplace source:

```bash
claude plugin marketplace add derogab/agent-kit
```

Then install the plugins you want:

```bash
claude plugin install git@agent-kit
claude plugin install sounds@agent-kit
```

## What\'s next

I plan to keep adding new pieces over time — anything that removes friction from repetitive workflows, and maybe some fun ones too.

If a skill saves even 30 seconds a day, it is nice to have and worth keeping.
