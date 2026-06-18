---
title: The Illusion of Doing
date: 2026-06-18 8:42:00
tags:
  - ai
  - software-development
  - technical-debt
  - productivity
  - team-velocity
---

AWS posted something that should make every engineering team stop and think.

> [More AI-generated code doesn\'t make your team faster. It might actually slow you down.](https://x.com/awscloud/status/2064449711155589396)
>
> — AWS ([@awscloud](https://x.com/awscloud))

But nobody is slowing down.

So\... what?!

In the age of AI, being fast has never been easier. With a prompt and a few seconds, you can generate thousands of lines of code, draft a full document, or produce a complete analysis. The tools are so good at amplifying personal output that it feels like you are accomplishing more than ever before. 

There is a dangerous illusion hiding in all this speed.

## Speed Is Not Progress

What feels like progress on a personal level does not always translate into progress for the company. An individual producing massive amounts of output can create the _impression_ that things are moving forward, while the company itself is barely advancing. **Speed without direction is just motion, not movement.**

AI has made it trivial to be fast as an individual. Responding instantly, generating code continuously, shipping pull requests by the dozen. All of this is now effortless. But the real risk is that you end up doing a lot of useless things. The volume masks the lack of alignment. You are busy, but you are not necessarily building what matters.

The real bottleneck was never writing code. It was releasing it, debugging it, and keeping it running well. That was true long before generative AI arrived. Writing more code faster does not solve any of these problems. It makes them worse.

> [AI makes typing cheaper, not ownership cheaper. If nobody can review, debug, and explain the code after, the team did not go faster, it just moved the bottleneck from writing to cleanup.](https://x.com/Prashtwtz/status/2064557767659332064)
>
> — Prashanth ([@Prashtwtz](https://x.com/Prashtwtz)), replying to AWS

## The Software Development Trap

This dynamic is especially visible in software development. It has become extremely easy to generate thousands of lines of code with AI assistants. The problem is that much of this code is useless or misaligned with the actual task at hand. The danger is writing code just to show that you are writing a lot. High volume, low utility.

Now we have the numbers to prove it. A [new NBER working paper](https://www.nber.org/papers/w35275) by Demirer, Musolff, and Yang tracked developer activity across GitHub and Microsoft telemetry, measuring the effect of AI coding tools at each stage of the production pipeline. The result is a cliff. Interactive coding agents produce a **741% increase in lines of code** written. But that number collapses at every subsequent stage: **+65% in pull requests**, and only **+20% in actual releases**.

Autocomplete shows the same pattern: 228% more lines of code, 36% more commits, 10% more releases. The authors call this the \"weak-link hypothesis\": AI\'s productivity gains at the writing stage are attenuated by human bottlenecks downstream. Code needs to be reviewed, integrated, tested, and released. AI does not do any of that. It just piles more work onto the humans who do.

Their model estimates an elasticity of substitution between AI output and human effort of just 0.25. AI and humans are (at least for now, obv.) strong complements, not substitutes. You cannot replace the human in the loop. You can only drown them in code they do not have time to review.

This is not a new problem: it\'s [Amdahl\'s Law](https://en.wikipedia.org/wiki/Amdahl%27s_law). Gene Amdahl noted in 1967 that speeding up one part of a computation has diminishing returns if the rest of the pipeline stays the same. For example, if code writing is 20% of the total development cycle, making it infinitely fast yields at most a 1.25x overall improvement — a 25% gain. The NBER paper finds the same dynamic: their model shows that with an elasticity of 0.25, even unlimited upstream AI yields only finite gains, and in practice those 741% more lines of code become just 20% more releases. Not 5x. Not 2x. Twenty percent.

A separate [large-scale study](https://arxiv.org/abs/2603.28592) shows where the fake-speed problem also becomes a reliability problem. Looking at over 300000 verified AI-authored commits across thousands of GitHub repositories, it found that more than 15% of commits from every major AI coding assistant introduced at least one issue. The illusion of clean, fast output does not hold up once you look under the hood.

> AI is an accelerant, an amplifier. It will not fix your systems for you. If your systems are already chaotic, all it does is inject more chaos into an already chaotic system.
>
> — [AWS for Software Companies Podcast Ep194](https://art19.com/shows/aws-for-software-companies-podcast/episodes/59a5e52f-411e-4017-9bd9-6dc0b9aee027), citing the [2025 DORA Report](https://dora.dev/research/2025/dora-report/)

And speed without reliability is just faster breakage.

## Technical Debt as a Compounding Tax

Worse than introducing issues is continuously adding absurd technical debt and a lack of understanding of the codebase. When you generate code faster than you can comprehend it, you are not building software. You are building the bottleneck that will slow everything down later.

The [arXiv paper 2603.28592](https://arxiv.org/abs/2603.28592) also tracked what happens to those AI-introduced issues over time: nearly a quarter of them (22.7%) were still present in the latest version of the repository. They had not been fixed; they persisted, accumulated, and became part of the codebase long after the original author had moved on. Out of 484366 distinct issues found in total, code smells alone accounted for almost 90%.

In the long term, this risks creating significant damage to the project. Speed without comprehension compounds into legacy problems that are expensive and painful to fix later. That quick feature that \"just works\" today becomes the bottleneck that slows down the entire team six months from now.

> The binding constraint is shifting from writing code to reviewing, integrating, and ultimately distributing it.
>
> — [NBER Working Paper #35275](https://www.nber.org/papers/w35275)

## The Vicious Cycle

Here is where the illusion turns into a trap. The technical debt generated by all that fast coding does not just sit there quietly. It amplifies the individual\'s useless speed by creating difficulties and critical issues that demand more effort to fix. You have to run faster just to stay in place.

Instead of growing, team velocity decreases. The more debt you accumulate, the more time the team spends firefighting instead of building. The company feels busy. Everyone is working hard. But real progress stalls. The illusion of doing becomes a self-reinforcing cycle of frantic activity and diminishing returns.

## What Actually Moves the Needle

True company velocity is not personal speed measured in lines of code. It comes from **team organization, shared decision-making, and agile development guided by a clear vision**.

> Every AI output has to have a human owner. If you don\'t want your name on it, it\'s probably not good piece of work.
>
> — [AWS for Software Companies Podcast Ep194](https://art19.com/shows/aws-for-software-companies-podcast/episodes/59a5e52f-411e-4017-9bd9-6dc0b9aee027)

Rules get gamed. Values create culture. When the standard is \"own what you ship\" rather than \"don\'t copy-paste AI output\", people think instead of complying.

This also means measuring the right things. If you track only lines of code or PRs merged, AI will flood those metrics while real progress stalls.

> It\'s worse to have just one or two metrics than to have no metrics. If you\'re going to have metrics, have a basket of them and look for the story they\'re telling you.
>
> — [AWS for Software Companies Podcast Ep194](https://art19.com/shows/aws-for-software-companies-podcast/episodes/59a5e52f-411e-4017-9bd9-6dc0b9aee027)

You need a basket of signals better than the number of PRs/commits/lines: **reliability, customer impact, deployment frequency, team velocity**. And the story they tell together, not any single number.

Less but better-targeted work outperforms sheer individual output every time. A small, well-understood change that solves the right problem creates more value than a massive refactor that nobody fully grasps. Company speed is a team property, not a personal metric.

## The Value of Thinking First

What is truly valuable is writing well-defined tasks and thoughtfully analyzing the best solution to reach a specific goal. This is far more important than writing a lot without thinking just to complete a task that \"works\" but will eventually break and make things much harder in the future.

Thinking before coding beats writing fast but fragile code. Understanding the problem beats generating a solution. A clear, shared goal beats individual heroics.

There is a longer-term risk here too. As AI makes code generation effortless, a generation of developers risks never learning to debug without it, reason about architecture, or truly understand what the code does. The productivity boost is real in the short term, but it creates a knowledge gap that compounds. AI-native developers risk becoming operators of black boxes rather than engineers who understand their craft. The output looks real. The understanding behind it is thin.

The quantity problem is solved. The quality problem has gotten harder than ever.

> Quality first, quantity second.
>
> — [AWS for Software Companies Podcast Ep194](https://art19.com/shows/aws-for-software-companies-podcast/episodes/59a5e52f-411e-4017-9bd9-6dc0b9aee027)

That sounds obvious until you realize how many teams operate the other way around: shipping as much as possible and hoping quality catches up later. With AI making volume free, the temptation to invert those priorities has never been stronger. **The differentiator is no longer who can produce the most. It is who can produce something worth owning.**

The illusion of doing is seductive because it feels productive. But real productivity is not measured in output volume. It is measured in meaningful progress toward the right outcomes. And that requires something AI cannot generate for you: judgment.

If you are going to put your name on it, make sure you understand it first.

![alt-text][header]

[header]: /assets/images/linked-to-posts/The-Illusion-of-Doing/header.png "The Illusion of Doing"
