# YouTube - Simon Scrapes - Every Level of Claude Code Explained in 39 Minutes

This [video](https://www.youtube.com/watch?v=Y09u_S3w2c8) explains the seven levels of Claude Code, guiding users from basic prompting to building fully autonomous systems.

Here's a breakdown of each level:

## Level 1: Planning before Execution (0:41-3:25)

* Emphasizes the importance of planning before execution to ensure Claude Code understands detailed requirements and assumptions.
* Introduces the "plan mode" for asking clarifying questions and building a comprehensive plan.md file.

## Level 2: Personalizing Claude for Better Responses (3:25-10:25)

* Focuses on using the claude.md file to provide Claude with rules, preferences, and details about your work style.
* Suggests keeping claude.md concise and referencing external files for detailed information (e.g., brand voice guidelines).
* Explains how to add and reload rules to refine Claude's output and avoid generic responses.

## Level 3: Slash Commands, Skills & Hooks - Repeatability (10:25-21:21)

* Slash Commands: Saved prompts for repetitive tasks, manually triggered with a single keystroke (e.g., /linkedin-post).
* Skills: Background knowledge loaded automatically when relevant, providing rich context without bloating the main claude.md file. Skills can be sourced from external repositories like Skills MP.
* Hooks: Automatic triggers that fire after Claude Code performs an action, useful for mechanical tasks like checking for "band words."

## Level 4: Connecting Claude Code to Your Apps (MCPs) (21:21-26:18)

* Demonstrates how to connect Claude Code to external applications like AirTable using "Multi-App Connectors" (MCPs).
* Shows how Claude can read data, create content based on that data, and update records within external apps.

## Level 5: Move from Executor to Supervisor (GSD Framework) (26:18-29:34)

* Introduces the GSD (Get Stuff Done) framework, which helps break down large projects into phases with detailed planning, execution, and verification steps.
* Addresses the "context rot" problem by keeping context in individual files and utilizing project documents (roadmap, requirements, state).

## Level 6: Agent Teams (29:34-35:57)

* Explains how to use specialized "sub-agents" to divide tasks, improve output quality, and increase processing speed.
* Discusses running agents in sequence for collaboration or in parallel for faster completion of non-dependent tasks.
* Introduces the dangerously-skip-permissions flag for autonomous operation (use with caution).

## Level 7: Fully Autonomous Systems (RALF Loop) (35:57-39:09)

* Describes the RALF (Run-Ask-Loop-Forward) loop, a bash script that enables Claude Code to continuously work until a specific condition is met.
* Requires a prd.json (product requirements document) file to define user stories and acceptance criteria for tasks.
* Differentiates RALF (executor for well-defined tasks) from GSD (planner and executor for larger, less defined projects).
