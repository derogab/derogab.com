---
title: "How an LLM writes our release notes without anyone noticing"
date: 2026-05-05 10:05:05
tags:
  - ai
  - github-actions
  - devops
  - waveful
---

Writing changelogs is boring, easy to forget, and always happens at the worst possible time. In a team that ships frequently — like ours at [Waveful](https://waveful.com) — it quickly becomes a chore you cannot ignore.

So we automated it.

![alt-text][action-preview]

## How it works (it\'s dumb simple)

[ChangelogAction](https://github.com/Waveful/ChangelogAction) is a GitHub Action that generates a `CHANGELOG.md` entry **on every new tag**. It pulls the merged PRs and commits since the previous release, packs them into a structured prompt, and lets an LLM write the actual changelog. The result is committed straight to your main branch.

If you want, it can also send a Telegram notification with a link to the updated file, and annotate the release in Mixpanel so your analytics stay in sync with deployments. Both are optional.

## The boring stuff, automated

The real reason we built this is simple: a language model is incredibly good at turning messy git history into readable text. PR titles, commit messages, file diffs — the LLM takes all of that noise and returns something coherent. No manual copy-paste, no forgotten changes, no Friday-evening rush.

It is the kind of text manipulation AI excels at, and it saves us time on every single release.

## Dogfooding it since day one

We have been running it on our repositories for months. Push a tag, wait a few seconds, and the changelog is ready.

It is open source under [Apache 2.0](https://github.com/Waveful/ChangelogAction/blob/master/LICENSE). If you ship regularly and have an LLM API handy, give it a try.

[action-preview]: /assets/images/linked-to-posts/Changelog-Action/action.png "Preview of the Changelog Action"