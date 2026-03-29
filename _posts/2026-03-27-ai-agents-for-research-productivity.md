---
layout: post
title: "UVA March 27 AI Agent Share Session"
date: 2026-03-27
description: "Notes from a March 27, 2026 UVA share session on Claude Code, RyanHub, and AgentOS."
---

On **March 27, 2026**, I gave a lab share session on how I use AI agents in day-to-day life and work.

The session was less about generic "AI productivity" and more about a change in how I think about software and daily workflows. What interests me now is not just asking a model for help in one isolated moment, but building systems that carry context, keep running after I stop typing, and start to feel like part of my working environment.

I started with a simple question: what does an AI-powered day actually look like? For me, that now includes things like automated parking, morning news and email triage, overnight paper review, experiment runs, software shipping, and background research workflows. None of those pieces is the whole story by itself. What matters is that they are beginning to connect into one continuous layer of support rather than a pile of disconnected demos.

From there, I spent a good portion of the talk on **Claude Code**, since it is the tool that made most of the rest possible. I focused on the parts that have mattered most in practice: long-lived sessions, reusable commands, MCP integrations, and `CLAUDE.md` as a kind of project memory. I also showed how I use it for concrete research work, from data analysis and experiment scripting to debugging and result parsing. What has made it useful for me is not just that it can write code, but that it can actually run things, inspect failures, and keep iterating until the workflow works.

I then talked about **RyanHub**, a personal AI iOS app that has gradually become a way for me to think through personal context, sensing, and interaction design. The core idea there is a shared context layer, which I call the **PersonalContext bus**. Instead of treating calendar, health, sensing, parking, and reading as separate silos, the app lets those modules feed into the same stream of context so the AI can reason across them. That is also why it feels closely connected to our lab's work: it is effectively a self-hosted sensing-and-intervention platform that I use in everyday life.

The other major thread was **AgentOS**, which is the clearest example I have right now of what happens when you keep pushing past one-shot prompting. I described it as a beta one-person company: a team of specialized agents with persistent roles, memory, routing, and review. What I wanted to emphasize was not the novelty of having many agents, but the fact that they can be organized, monitored, and made accountable. Once you add handoffs, memory, and review layers, agents start to behave less like disposable chats and more like an operating structure.

I ended with a few mindset shifts that have felt increasingly important to me. One is moving from **executor to leader**: spending less time doing everything myself and more time directing systems well. Another is moving from isolated **tools to systems**: getting value not from a single clever command, but from shared context and composition. And the third is moving from **sessions to institutions**: if agents can accumulate memory and operate within stable workflows, they begin to build continuity over time instead of resetting to zero.

If there was a single theme across the whole session, it was that I am less interested in AI as a smarter interface and more interested in AI as infrastructure: something that can coordinate work, carry context, and become part of the environment in which research and daily life happen.

If you want the full deck, it is available here:

- [UVA March 27 AI Agent Share Session (PDF)]({{ '/ai-agents-for-research-productivity.pdf' | relative_url }})

In that sense, the talk sat across both sides of my current work. RyanHub reflects my interest in personal context, sensing, and health-related AI systems. AgentOS reflects my interest in building agent infrastructure that is reliable, inspectable, and usable in the real world.
