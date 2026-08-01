---
title: "AI Notes: record, transcribe, enrich"
date: 2026-08-01 17:34:37
tags:
  - ai
  - open-source
  - obsidian
  - privacy
  - self-hosted
---

It\'s absurd, if you think about it. People record their most private thoughts (therapy notes, business ideas, things they wouldn\'t say out loud in a crowded room) into proprietary, closed-source apps that ship every word to servers on the other side of the world. Nobody knows what happens there. Nobody can know: the code is closed. And we just\... accept it?

Open source alternatives were born, of course. And they were great, at least in their initial phase. Minimal, focused, honest. But most of them are startups, and startups have to grow. So features pile up. Paid tiers appear. The roadmap stops serving the user and starts serving the pitch deck. And today, with AI, it has never been easier to keep shipping AI-slopped features. Seriously, it\'s a note enhancer! What else is it supposed to do?!

Because the thing itself is very simple:

- record locally
- transcribe with a local system
- enrich with local LLMs

That\'s the whole product. Everything else is noise.

## AI Notes

So I built [AI Notes](https://github.com/derogab/ai-notes), a minimal Obsidian plugin that records audio, transcribes it, and enriches your notes. It was recently published as an [Obsidian community plugin](https://community.obsidian.md/plugins/ai-notes), so you can install it directly from Obsidian.

<img src="/assets/images/linked-to-posts/AI-Notes/preview.gif" alt="AI Notes preview" title="AI Notes preview" style="width:100%;">

## Minimalism by design

The plugin does as little as possible. It just aggregates pieces that already exist:

- **Obsidian** manages everything as plain markdown files, on your disk.
- **The plugin** records audio, and the audio stays local, embedded next to your note.
- **Transcription** sends the audio to any Whisper-compatible server, including one running on your own machine.
- **Enrichment** connects to any OpenAI-compatible server, again including a local one (llama.cpp, DwarfStar, Ollama, LM Studio, whatever you like).

Totally self-manageable. Everyone can wire up the endpoints based on their own needs: fully local and private, self-hosted on your home server, or a cloud API if that\'s the trade-off you consciously choose. The point is that _you_ choose. Nothing leaves your machine unless you decide it should.

That\'s all. No account, no telemetry, no premium tier, no AI copilot sidebar assistant agent whatever.

Sometimes what you need is just a plugin developed over a weekend, not software with billions in valuation.

It\'s open source under GPL-3.0. [Give it a try](https://community.obsidian.md/plugins/ai-notes).

## Links

<table>
<tr>
  <td>Source Code</td>
  <td><a href="https://github.com/derogab/ai-notes" target="_new">GitHub Repository</a></td>
</tr>
<tr>
  <td>Obsidian Community Plugin</td>
  <td><a href="https://community.obsidian.md/plugins/ai-notes" target="_new">AI Notes</a></td>
</tr>
</table>
