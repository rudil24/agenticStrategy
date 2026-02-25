# Claude Code Hooks

Claude Code hooks are programmable triggers that allow you to execute custom commands or LLM prompts at specific points within Claude Code's lifecycle, either *before* or *after* various events. This provides deterministic control over the AI's behavior, ensuring certain actions are consistently performed.

These hooks can be configured to respond to a wide array of events, offering flexibility in automating workflows and enforcing standards.

Here is a quick breakdown of the types of hooks supported:

## 1. Before Events (Pre-Hooks)
These are executed prior to the event taking place.
*   __`PreToolUse`__: Triggers before Claude executes a tool (like running a command or writing to a file). This is often used to validate or block dangerous operations.
*   __`UserPromptSubmit`__: Triggers when you submit a prompt, *before* Claude even starts processing it (great for injecting context).
*   __`PreCompact`__: Triggers before context compaction.

## 2. After Events (Post-Hooks)
These are triggered after an event completes.
*   __`PostToolUse`__: Triggers after Claude successfully runs a tool (good for auto-formatting code or running tests).
*   __`PostToolUseFailure`__: Helps handle errors after a failed tool call.
*   __`Stop` / `SubagentStop`__: Fires when Claude or a subagent finishes a response.

## 3. Lifecycle Events
These trigger based on the session's overall lifecycle.
*   __`SessionStart` / `SessionEnd`__: Triggered when a Claude Code session begins or closes.
*   __`Notification`__: Triggered when Claude Code sends a notification.
