---
layout: post
title: "UVA March 27 AI Agent Share Session"
date: 2026-03-27
description: "Notes from a March 27, 2026 UVA share session on Claude Code, RyanHub, and AgentOS."
---

On **March 27, 2026**, I gave a lab share session on how I use AI agents in day-to-day life and work.

The talk was not mainly about generic "AI productivity." It was about a broader shift in how I think about personal systems, research workflows, and software execution: moving from one-off chat interactions toward persistent agents, shared context, and systems that can keep working after I stop typing.

I opened with an intentionally concrete hook: an AI-powered day in my own life. That included automated parking, morning news and email triage, overnight paper review and experiment runs, product shipping through my own agent stack, and an auto-research workflow running in parallel. The point was not that each demo is individually impressive. The point was that these workflows are starting to compose into a coherent operational layer.

From there, the session moved through four parts:

1. **Claude Code** as the base agent runtime.
I walked through the parts of Claude Code that matter most in practice: long-lived sessions, large context windows, reusable slash commands, MCP integrations, and `CLAUDE.md` as project memory. I also showed how I use it for real research work such as data analysis, experiment scripting, results parsing, and iterative debugging. A key point here was that Claude Code is useful not just because it writes code, but because it can run commands, inspect outputs, and iterate autonomously until something actually works.

2. **RyanHub**, a personal AI iOS app.
I presented RyanHub as a personal AI super-app built around a hub-and-spoke architecture: AI chat at the center, with modules for calendar, health, passive sensing, parking, and reading. The most important idea was the **PersonalContext bus**. Instead of treating each feature as a separate app, every module writes to a shared context layer, and the AI reads across that layer to form personalized, cross-module understanding. This is also why the app is relevant to our lab's research interests: it is a real, self-hosted sensing-and-intervention platform running on a person's phone every day.

3. **AgentOS**, a beta one-person company.
The second large demo was AgentOS, which I described as what happens when you push Claude Code to the limit. Here the framing was organizational rather than app-centric: a team of specialized agents with persistent roles, tracked work, institutional memory, and human oversight. I showed how issues flow through the system, how agents hand work off, how memory survives across sessions, and how quality control works through a three-stage review structure. The point was not "multi-agent theater," but how role separation, routing, review, and memory turn disposable agents into something closer to an operating organization.

4. **Mindset shifts**.
I closed with three shifts that I think matter more than any specific tool choice: moving from **executor to leader**, from isolated **tools to systems**, and from individual **sessions to institutions**. If agents can accumulate memory, read shared context, and operate inside repeatable workflows, then the question stops being "what prompt should I use?" and becomes "what kind of system am I building?"

If you want the full deck, it is available here:

- [UVA March 27 AI Agent Share Session (PDF)]({{ '/ai-agents-for-research-productivity.pdf' | relative_url }})

In that sense, the session sat across both sides of my current work. RyanHub reflects my interest in personal context, sensing, and health-related AI systems. AgentOS reflects my interest in building agent infrastructure that is reliable, inspectable, and usable in the real world.
