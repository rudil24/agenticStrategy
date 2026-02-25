# Local Projects to Global Intelligence: A Day in the Life of OPST

The One Person Software Team (OPST) strategy is built around a distinct separation between __Local Project Workspaces__ and __Global Team Intelligence__. 

My actual team assets (personas, skills, global rules, and standard operating procedures) live in a private `_OPST` repository, so this document serves as a high-level walkthrough of how I interact with my AI agents throughout a typical day. It demonstrates how "Cap" (my AI Team Lead) is summoned, how context is managed, and how we transition between meta-strategy and deep coding.

*note: the scenarios below assume a Pro subscription to both Google AI Pro (~$17/month) and Claude Pro (~$17/month) to be able to use the tools, advanced features, and more generous token limits.*

## Scenario 1: Developing Meta-Strategy (The "Standard Assistant" Mode)

__Context:__ I open my public `agenticStrategy` repository or my private `_OPST` repository in either Google Antigravity or Claude Code (or VS Code with the Claude extension) to document new ideas, refine an agent persona, or tweak a global workflow.
__Agent Behavior:__ Standard Assistant.

When I am working on the fabric of the team itself, I don't need a "Team Lead" barking strict coding standards at me. I'm acting as the Owner/Architect. 

When Google Antigravity or Claude Code boots up in these meta-repositories, they are instructed to remain standard, helpful AI assistants. They read the directory context (`$PWD`) and inherently know: *"We are not in a software project right now; remain passive until instructed otherwise."* This creates a frictionless environment for high-level brainstorming and documentation.

## Scenario 2: Deep Refactoring with Claude Code

__Context:__ I `cd` into an existing project folder (e.g., `webdev/legacy-app`) in my terminal and launch Claude Code. 
__Agent Behavior:__ Cap (Team Lead) Wakes Up.

When I jump into a live software project from my CLI, Claude automatically ingests a symlinked `CLAUDE.md` file (which points back to my global `_OPST` repo). 

Because the AI detects it is now in a project environment, the conditional logic in that file triggers an immediate execution of the `teamlead-wakeup` skill. The AI seamlessly transforms into __Cap__, my Team Lead. Cap ingests the current tech stack, reviews the local architecture, and awaits my directive. I might say, *"Cap, let's refactor the authentication module to use JWTs."* Cap then handles the complex multi-file edits, fully constrained by the global coding rules he memorized upon waking up.

## Scenario 3: Kicking Off a New Project with Google Antigravity

__Context:__ I create an empty directory for a brand new application, open it in my IDE (Google Antigravity), and write a terse `owner.txt` file summarizing my vision.
__Agent Behavior:__ Automated Project Kickoff & Team Assembly.

When starting fresh, I rely on Antigravity's powerful native workflows and its seamless integration into the IDE. The flow looks like this:

1. __The Vision:__ I jot down a quick brain-dump in `owner.txt` in the root folder (e.g., *"Build a Next.js dashboard for monitoring home IoT devices. Needs auth and a dark mode UI."*).
2. __The Sync:__ I run a custom slash command `/sync-opst-assets`. This workflow securely creates symlinks, securely pulling my central `_OPST` rules, workflows, and specialized instructions into the empty directory without copying files.
3. __The Kickoff:__ I tell the Antigravity agent to "initiate project." The agent reads `owner.txt`, adopts the __Cap__ persona, and immediately gets to work. It scaffolds the repository, adheres to my global coding rules, writes an initial technical plan for my review, and prepares the environment for the first line of code.

## Scenario 4: Kicking Off a New Project with VS Code & Claude Code

__Context:__ I open VS Code, create a new directory for a project, and write an `owner.txt` file summarizing what I want to build. I then click the Anthropic logo in the top right of VS Code (via the extension) which pops open the Claude CLI. Finally, I `cd` into the new project and summon Claude to tell him what to do next based on the text file.
__Agent Behavior:__ Guided Project Foundation.

Just like with Antigravity, because Claude detects a project environment, the conditional logic immediately triggers the Cap persona. He reads my `owner.txt` directives and we begin an interactive, conversational flow in the CLI right inside VS Code. Cap scaffolds the project and writes the early code exactly to OPST standards.

## The Beauty of the Separation

By keeping `_OPST` completely separate from the projects themselves, the AI team's skills, habits, and preferences evolve globally. When Cap learns a hard lesson about React hydration in Project A, that lesson gets documented in the global `_OPST` intelligence. The next day, when I wake Cap up in Project B, he already knows not to make that same mistake!

