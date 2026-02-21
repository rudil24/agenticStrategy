# Claude Code Agent Teams: A One-Page Summary

*Based on the concepts from ["Learn 90% Of Claude Code Agent Teams in 22 Minutes"](https://www.youtube.com/watch?v=cSkoaCCmq0w) and official Claude Code documentation.*

**Agent Teams** are an experimental, advanced feature in Claude Code that enables multiple AI agents to collaborate simultaneously on a single project, mimicking a human development team. They go beyond simple "subagents" by allowing for true parallel execution and inter-agent communication.

## 1. Core Concepts & Operational Model

- **Team Lead vs. Teammates:** When you initiate a team, your main Claude instance becomes the "Team Lead." It orchestrates the overarching goal, breaks down the work into a shared task list, assigns specific pieces to specialized "teammates," and synthesizes their final results.
- **Parallel Work & Shared Context:** Unlike subagents (which usually run sequentially and only report back to the main agent), teammates operate independently within their own context windows, work on different parts of the problem concurrently, and can communicate with each other.

## 2. When to Use Agent Teams

Agent Teams shine in scenarios that highly benefit from parallel processing or multi-angle investigation:

- **Deep Debugging:** Having multiple agents investigate different hypotheses for a stubborn bug simultaneously.
- **Massive Refactors:** Splitting up a large feature development where different agents tackle the frontend, backend, and database schema at the same time.
- **QA Swarms:** Setting up multiple agents to aggressively test different edge cases of a newly built feature concurrently.
*(Note: For simple, linear tasks or pure research, standard Subagents are usually more appropriate and cost-effective).*

## 3. Display Modes

You can view your Agent Teams working in two different ways:

- **In-Process Mode:** All teammates run within your single terminal window. You cycle through them to see what each is doing.
- **Split-Panes Mode:** (Highly recommended for visibility). Using terminal multiplexers like **tmux** or **iTerm2**, Claude automatically splits your screen into multiple panes so you can literally watch 4 or 5 agents typing code in parallel.

## 4. Setup & Invocation

1. **Enable the Flag:** Because it is an experimental feature, you must ensure your Claude Code is up to date and you have enabled the necessary experimental flags in your settings.
2. **Terminal Prerequisites:** If you want Split-Panes mode, ensure `tmux` or `iTerm2` is installed and configured on your machine.
3. **Execution:** You can trigger a team simply by asking Claude to "create a team" for a specific complex task. If a task naturally benefits from parallelization, Claude may proactively suggest spinning up a team.

## 5. Crucial Considerations & Trade-offs

- **Exponential Token Costs:** This is the biggest catch! Because each teammate maintains its own *full* context window of the project, token usage can easily be **2x to 4x higher** than a single-agent workflow. Use teams surgically.
- **Diminishing Returns:** The optimal team size peaks at around **5 to 6 agents**. Beyond that, the overhead of coordination outweighs the benefits.
- **File Collision Risk:** While powerful, having multiple agents working in parallel means occasionally two agents might try to overwrite or refactor the exact same file simultaneously.

---
*Tip: Always weigh the speed boost of a Team against the token cost. Use the `GSD (Get Stuff Done)` or `Ralph` loop frameworks for sequential autonomy, and reserve Agent Teams for high-complexity parallel swarms!*
