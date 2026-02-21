---
title: "Building things with AI. Product management. Woodworking. Writing."
date: 2026-02-20
draft: false
tags: [ai, agents, management, series]
authors: ["Geoff Dudgeon", "Claude Opus", "Spiral"]
summary: "The best book on managing AI agents was published in 2023 and never mentions artificial intelligence. Part one of a series applying Claire Hughes Johnson's Scaling People to agent builders."
---

The best book on managing AI agents was published in 2023, runs 480 pages, and never once mentions artificial intelligence.

It's called Scaling People. Claire Hughes Johnson — former VP at Google, former COO of Stripe — wrote it as the definitive playbook for building and managing high-performing human organizations. Hiring, team development, feedback systems, operating principles, organizational design. Battle-tested frameworks from two of the most consequential companies in tech.

I picked it up to get better at managing people. I put it down thinking about agents.

Not in a hand-wavy "agents are like people too" way. In a structural, operational way. The problems Hughes Johnson solves — alignment, coordination, quality at scale, role clarity, communication breakdown — are the exact problems agent builders face today. Her solutions transfer more directly than you'd expect.

This is the first in a four-part series that makes the translation explicit. Each post takes a core section of the Scaling People framework and converts it into actionable guidance for agent builders. Concrete mental models, not metaphors. Diagnostic tools you can actually use.

It starts with a framework I now use to think about every agent I build.

## Five forces that shape every agent

Ask a manager what shapes an employee's behavior, and you'll get a familiar list: culture, training, resources, processes, information.

Ask an agent builder the same question, and you'll get a technical list: system prompt, model capabilities, tool integrations, orchestration logic, context window.

Same five forces. Different vocabulary.

I call them the five steering mechanisms — a framework that bridges management language and engineering language so both sides can reason about agent behavior together.

### Rules (i.e. CLAUDE.md/AGENTS.md) → Culture and values

Hughes Johnson argues that strong culture enables autonomy. People make better decisions without supervision when values are clear and internalized.

For agents, Rules are the explicit encoding of this: system prompts, guardrails, access policies, output constraints. They define the boundaries. More importantly, they define principles — how the agent should handle ambiguity, make tradeoffs, and behave in situations its instructions don't cover.

Most teams write system prompts as procedures. The better frame is culture: "Here's what we value. Here's what's off-limits. Here's how we make tradeoffs when goals conflict." Agents with clear principles handle novel situations better — not because they're smarter, but because they have something to reason from beyond rote instructions.

### Skills (i.e. SKILLS.md) → Training and development

In Scaling People, capability building is ongoing. You don't stop training someone after their first week. And crucially, the investment compounds — skills developed in one context transfer to the next.

Agent skills work the same way, but with two differences that make the process faster and more reliable. The first is speed of propagation. A prompt or SKILL.md refinement that teaches an agent better reasoning applies immediately, across every subsequent run. Improve a shared agent skill and every agent that inherits it gets better at once. The investment scales in ways human training simply can't match.

The second difference is reliability of transfer. When a manager coaches a human report through a recurring mistake, there's no guarantee it sticks — memory is imperfect, old habits reassert. With agents, you write the improvement into a persistent skills document the agent reads at the start of every run, and it follows it. Every time. The lesson doesn't fade under pressure or revert after a long weekend. The transfer mechanism is write, not teach.

That reliability also extends to self-assessment. Skilled managers can get candid reflection from their reports — but it takes time, trust, and careful framing. With agents, you ask directly: "what went wrong in that last run, and how would you approach it differently?" No ego to manage, no career anxiety to navigate. The conversation that takes a skilled manager three one-on-ones to have takes three seconds. That doesn't make the agent better at its job. It makes the improvement cycle faster.

### Workflows → Processes and systems

Hughes Johnson's core argument on process: it's not bureaucracy, it's how you scale without chaos. Processes encode decisions so they don't have to be relitigated every time. They make coordination possible.

For agents, Workflows are the orchestration layer — chains, routing logic, handoff protocols, escalation paths. They define what happens in what sequence, under what conditions, and in coordination with which other agents or humans.

The same tension from human orgs applies: premature process kills agility, absent process kills quality. An over-orchestrated agent system is brittle. An under-orchestrated one is unreliable. Finding the right level of structure is ongoing management work.

### Context → Information and communication

Hughes Johnson's sharpest observation about organizations: most dysfunction traces to information failure. People making decisions without the information they need to make them well.

For agents, Context is the information available at the moment of decision — conversation history, retrieved documents, memory, user state. It's the most neglected of the five mechanisms. Teams invest heavily in Rules (prompt engineering) and Tools (integrations) while starving agents of the Context they need to use those rules and tools effectively.

An agent without proper context is a new hire setting strategy before anyone's told them what the company does. The output might be articulate. It won't be correct.

## Diagnosis over debugging

Here's why this framework matters beyond taxonomy.

When an agent produces bad output, most teams reach for the same two levers: rewrite the prompt or try a different model. That's the equivalent of sending every underperforming employee to the same generic training — occasionally helpful, usually beside the point.

The five steering mechanisms turn "it's not working" into a diagnostic question:

- Agent violated a constraint? → Rules. Sharpen the guardrails.
- Agent couldn't execute? → Skills. Develop the capability.
- Agent lacked needed capability? → Tools. Expand or reconfigure the tool set.
- Work went down the wrong path? → Workflows. Fix the orchestration.
- Agent decided without key information? → Context. Fix retrieval, memory, or state management.

Five root causes, five different interventions. Each maps to a concept any stakeholder can understand. That shared vocabulary is itself a management tool — it lets engineering, product, and operations teams reason about agent performance in a common language, the way Hughes Johnson's frameworks give cross-functional teams a shared language for people management.

## This is just the foundation

The five mechanisms give you a way to reason about individual agent behavior. But Scaling People covers far more than individual management — it's a book about organizational design, team composition, operating rhythm, and feedback systems.

The rest of this series goes just as deep:

Next up: Building your agent org. Hughes Johnson's frameworks for operating principles, planning cadences, and retrospectives translate directly. Your agent system needs a mission statement — not as a thought exercise, but as a practical alignment tool. Your agent org needs a retrospective rhythm — because compounding failures in agent systems are invisible until they're catastrophic. I'll show what these look like when the "organization" is software.

Then: Hiring and team design. Agent selection mirrors hiring in ways that reshape how you build. When should you deploy a specialist agent vs. a generalist? How do you compose multi-agent ensembles that genuinely coordinate? Hughes Johnson's team-design principles provide answers that are more nuanced — and more practical — than "just add another agent to the chain."

Finally: Feedback, performance, and where the analogy breaks a little. Evals are the agent equivalent of performance reviews, and they're implemented about as well as most companies run annual reviews — inconsistently, infrequently, and with unclear standards. We'll cover what good feedback loops look like for agents, the emerging shape of the agent-augmented worker, and an honest accounting of where this entire management frame stops working. The places where agents aren't like people reveal as much as the places where they are.

The premise of this series is simple: you don't need to invent a management science for AI agents from scratch. The hardest problems — alignment, coordination, quality at scale — have been worked out before, in a different domain. This series does the translation.
