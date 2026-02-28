# The Bits and Bytes of OPST

Where do my tooling assets live? Where does my source code live? How and where do I deploy source and birth the babies?

## Digital Footprint (for Building Code)

As you can see in the graphic below, I've uncoupled the team assets from the project assets, to make sure the learning flows up and out of the projects and into the team.

![Build Digital Footprint](buildFootprint.svg)

* The root or home workspace (mine is called `webdev`) has a distinction between the `_OPST` team repository and the individual projects they build. That way, the team advancement is decoupled from the project(s) themselves.
  * the folder is "underline OPST" because I like it showing up at the top of my workspace folder list in my browser/terminal/IDE
* A `GLOBAL_EVOLUTION.md` (name is arbitrary, that's just what Gemini suggested and we went with it) tracks the evolution of the team's skills and capabilities, preferences, etc.
* A `CLAUDE.md` is there to orient Claude that he isn't the only show in town and that `GLOBAL_EVOLUTION.md` is the ultimate rulemaker

### Team Assets

Here's a breakdown of what you'll find in the OPST assets:

* __AGENTS__: Defines the personas, roles, and instructions for the different AI team members.
* __DOCS__: Contains global documentation, templates (like PRDs), and architecture standards shared across projects.
* __MCPs__: Holds Model Context Protocol definitions (and json snippets to connect to external MCP Servers) to securely connect the agents to external tools, databases, and APIs.
  * See a [great catalog of available MCP Servers across the world](https://www.pulsemcp.com/servers)
* __SKILLS__: A library of instructions and resources that extend the team's capabilities for specialized, complex tasks.
  * See the [amazing agent skills people are creating](https://skillsmp.com/)
* __RULES__: __(Google Antigravity specific)__ Global rules of engagement, constraints, and coding standards that the agent automatically reads. *(Analogous to Claude's Project Knowledge or Custom Instructions).*
* __WORKFLOWS__: __(Google Antigravity specific)__ Well-defined, step-by-step repeatable processes (like project kickoffs) that the agent can auto-run. *(Analogous to step-by-step task lists or standard operating procedures given to Claude).*
* __COMMANDS__: __(Claude specific)__ Standardized CLI commands, slash commands, or custom tools defined for Claude to quickly automate actions. *(Analogous to Antigravity's native `run_command` scripting or custom Agent Skills).*
* __HOOKS__: __(Claude specific)__ Automation triggers that run [before or after](claudeHooks.md) certain actions during the development lifecycle. *(Analogous to automated steps grouped directly into Antigravity Workflows).*

*(Note: AGENTS, DOCS, MCPs, and SKILLS are assets that BOTH Claude and Google Antigravity "fw" / utilize together.)*

> I've gotta say, the assets discovery of this OPST strategy has been an amazing, delightful experience in 2026.  
> Apparently I'm not the only person to think that it would be cool to have AI agents accrue skills,  
> and find ways to naturally make connections between themselves. /s

### Symlinking for instant global read/writes on either stack

In any project the team starts, I have a workflow that symlinks the AI rules of engagement (CLAUDE.md) and (.agent/rules) and (.agent/workflows) for that folder into the OPST assets folder. This way, the team can rely on a single source of truth for the AI rules of engagement and workflows, and can easily update them from either stack.

Here's what that translates to in a [typical workday](localToGlobal.md).

## Digital Footprint (for Deploying Code)

![Deploy Digital Footprint](deployDF.svg)

I'm proficient (cough, cough) in Javascript PERN stack, and Python/Flask stack. So my source code can utilize either of those stacks to deploy to the cloud.

### Client side Javascript Only - GitHub Pages

I can deploy client side Javascript code to GitHub Pages, FOR FREE UNLIMITED, [even if i'm using React+Vite in the front-end](reactViteSurvivalGuide.md). The only stipulation is not to have any Node/Express/Postgres dependencies. So that's my go-to for that type of project.

### PERN or Python/Flask Full Stack demo

I have a $6/month database set up with Render.com (just so they don't flush the database every 30 days), and I set up the database partitioned so I can just add new projects with new partitions and not buy a new database every time. You could do this for free too, as long as you don't mind them wiping customer data every 30 days. The only downside of this setup is since I'm too cheap to buy the pro plan that gets you a spun-up web server ($20/month), my demo customers get the "app booting up" as a user experience. (sometimes lasts up to a minute).

### PERN stack "grow into production"

I've heard exciting things about Railway.com, so I think that'll be what I try when I "just know" I have a production hit on my hands, and I want it to grow from $5/month to wherever it needs to go.  Hopefully it doesn't turn out like [jmail.world on Vercel](https://www.reddit.com/r/webdev/comments/1r3cplc/jmailworld/)]

### Serverless? Maybe someday

I'll cross that bridge (AWS, GCP, Azure, etc) when I come to it. That's a lot more DevOps than I'm ready for right now.

Here's a bit more detail from Gemini who I sent on a [fact-finding mission about hosting](appHosting.md).
