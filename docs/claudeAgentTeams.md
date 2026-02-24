# Claude Code Agent Teams: A One-Page Summary

*Based on the concepts from ["Learn 90% Of Claude Code Agent Teams in 22 Minutes"](https://www.youtube.com/watch?v=cSkoaCCmq0w) and official Claude Code documentation.*

__Agent Teams__ are an experimental, advanced feature in Claude Code that enables multiple AI agents to collaborate simultaneously on a single project, mimicking a human development team. They go beyond simple "subagents" by allowing for true parallel execution and inter-agent communication.

## 1. Core Concepts & Operational Model

- __Team Lead vs. Teammates:__ When you initiate a team, your main Claude instance becomes the "Team Lead." It orchestrates the overarching goal, breaks down the work into a shared task list, assigns specific pieces to specialized "teammates," and synthesizes their final results.
- __Parallel Work & Shared Context:__ Unlike subagents (which usually run sequentially and only report back to the main agent), teammates operate independently within their own context windows, work on different parts of the problem concurrently, and can communicate with each other.

## 2. When to Use Agent Teams

Agent Teams shine in scenarios that highly benefit from parallel processing or multi-angle investigation:

- __Deep Debugging:__ Having multiple agents investigate different hypotheses for a stubborn bug simultaneously.
- __Massive Refactors:__ Splitting up a large feature development where different agents tackle the frontend, backend, and database schema at the same time.
- __QA Swarms:__ Setting up multiple agents to aggressively test different edge cases of a newly built feature concurrently.
*(Note: For simple, linear tasks or pure research, standard Subagents are usually more appropriate and cost-effective).*

## 3. Display Modes

You can view your Agent Teams working in two different ways:

- __In-Process Mode:__ All teammates run within your single terminal window. You cycle through them to see what each is doing.
- __Split-Panes Mode:__ (Highly recommended for visibility). Using terminal multiplexers like __tmux__ or __iTerm2__, Claude automatically splits your screen into multiple panes so you can literally watch 4 or 5 agents typing code in parallel.

## 4. Setup & Invocation

1. __Enable the Flag:__ Because it is an experimental feature, you must ensure your Claude Code is up to date and you have enabled the necessary experimental flags in your settings.
2. __Terminal Prerequisites:__ If you want Split-Panes mode, ensure `tmux` or `iTerm2` is installed and configured on your machine.
3. __Execution:__ You can trigger a team simply by asking Claude to "create a team" for a specific complex task. If a task naturally benefits from parallelization, Claude may proactively suggest spinning up a team.

## 5. Crucial Considerations & Trade-offs

- __Exponential Token Costs:__ This is the biggest catch! Because each teammate maintains its own *full* context window of the project, token usage can easily be __2x to 4x higher__ than a single-agent workflow. Use teams surgically.
- __Diminishing Returns:__ The optimal team size peaks at around __5 to 6 agents__. Beyond that, the overhead of coordination outweighs the benefits.
- __File Collision Risk:__ While powerful, having multiple agents working in parallel means occasionally two agents might try to overwrite or refactor the exact same file simultaneously.

---
*Tip: Always weigh the speed boost of a Team against the token cost. Use the `GSD (Get Stuff Done)` or `Ralph` loop frameworks for sequential autonomy, and reserve Agent Teams for high-complexity parallel swarms!*
