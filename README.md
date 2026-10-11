# dont-be-so-lapalissian

I didn't make this to save tokens, but because I keep getting pissed off when AI talks to me like that.

A writing skill that helps AI assistants state their point directly. It removes redundant negative qualifications, obvious exclusions, and unnecessary contrasts while preserving meaningful caveats, uncertainty, and distinctions that affect understanding or action. Includes contextual examples and a practical editing checklist.

Read [SKILL.md](SKILL.md) for the complete instructions and examples.

## How to install

The skill is a plain-text instruction file called `SKILL.md`.

### 1. Download it

Click **Code → Download ZIP** at the top of this repository, then extract the ZIP. Open the extracted folder: it contains `SKILL.md` and this README.

### 2. Put it where your agent looks for skills

Create a folder named `dont-be-so-lapalissian` in one of the locations below, then copy `SKILL.md` into it. Create any missing folders.

| Agent | Personal installation (across local projects) | Installation for one project |
| --- | --- | --- |
| Codex | `~/.agents/skills/dont-be-so-lapalissian/` | `.agents/skills/dont-be-so-lapalissian/` |
| Claude Code | `~/.claude/skills/dont-be-so-lapalissian/` | `.claude/skills/dont-be-so-lapalissian/` |
| GitHub Copilot | `~/.copilot/skills/dont-be-so-lapalissian/` | `.github/skills/dont-be-so-lapalissian/` |

`~` means your home folder: for example, `C:\Users\YourName` on Windows or `/Users/YourName` on macOS. Project paths start inside your project's main folder. Enable hidden-file visibility if folders beginning with a dot are hidden.

For example, a personal Codex installation on Windows should contain:

```text
C:\Users\YourName\.agents\skills\dont-be-so-lapalissian\SKILL.md
```

Personal folders apply to agents running on that machine. For cloud agents, use the supported project location and commit the skill to the project repository. Other agents supporting the Agent Skills format can use the same file in their documented skills directory.

### 3. Activate it

Start a new agent session and ask:

> Read and apply the dont-be-so-lapalissian skill to all your responses in this conversation.

In Codex, you can also mention `$dont-be-so-lapalissian`; in Claude Code, use `/dont-be-so-lapalissian`.

To make it a standing preference, add the following to your agent's persistent instructions, replacing `PATH` with the actual location of the installed file:

> At the start of each conversation, read PATH/SKILL.md and apply dont-be-so-lapalissian to all user-facing responses and original prose. State the intended meaning directly; remove redundant negative qualifications while preserving useful caveats and distinctions.

Use `~/.codex/AGENTS.md` for personal Codex instructions, `~/.claude/CLAUDE.md` for personal Claude Code instructions, or your agent's custom-instructions settings. Append this preference to existing instructions. Installing a skill makes it available; the persistent instruction requests its ongoing use.

### Using it in other AI chats

If your app accepts custom instructions, copy the body of [SKILL.md](SKILL.md), starting at the `# dont-be-so-lapalissian` heading, into that setting. For a single conversation, paste it into the chat and ask the assistant to apply it throughout the conversation. If the settings field is too short, use:

> State what you mean directly. Remove redundant negative qualifications and exclusions already obvious from context. Keep distinctions that answer a real question, correct a misunderstanding, or communicate relevant limits and uncertainty.

Persistence depends on the app's instruction and memory features.

Official setup references: [Codex](https://learn.chatgpt.com/docs/build-skills), [Claude Code](https://code.claude.com/docs/en/skills), and [GitHub Copilot](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills).
