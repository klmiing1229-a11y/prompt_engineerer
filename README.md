# LFG — Prompt Engineer On Call

Turn a rough idea into a clear prompt, review it, then have your AI carry it out. Start a message with `lfg`:

```text
lfg write a friendly welcome email for new customers
```

The assistant drafts a prompt and pauses. Reply `ok` to run it, describe a change to revise it, or say `just the prompt` to copy it elsewhere.

## What is in this repo?

| File | Use it for |
| --- | --- |
| [`lfg/SKILL.md`](lfg/SKILL.md) | The complete skill from the original `.skill` package, written for Claude. |
| [`PORTABLE.md`](PORTABLE.md) | A shorter, model-neutral version for custom or project instructions. |

The full skill includes a prompt template, formatting rules, examples, and the review-and-approval workflow. Its Opus/Sonnet guidance is specific to Claude. Use the portable version if your AI does not offer those models.

## Install the full skill

### Claude Code

1. Download this repository or copy [`lfg/SKILL.md`](lfg/SKILL.md).
2. Put it at `~/.claude/skills/lfg/SKILL.md` for all your projects, or at `<your-project>/.claude/skills/lfg/SKILL.md` for one project.
3. Start a new Claude Code session. Try `lfg draft a short product description for a travel mug` (or invoke `/lfg`).

See the [Claude Code skill documentation](https://code.claude.com/docs/en/skills) for skill locations and invocation.

### Codex

1. Download this repository or copy [`lfg/SKILL.md`](lfg/SKILL.md).
2. Put it at `~/.agents/skills/lfg/SKILL.md` for personal use, or at `<your-project>/.agents/skills/lfg/SKILL.md` for one repository.
3. Ask Codex to use the `lfg` skill, or invoke `$lfg`. If you want the drafted prompt to target a model other than Claude, name that model in your request.

See the [Codex skill documentation](https://learn.chatgpt.com/docs/build-skills) for local skill locations.

## Use it with ChatGPT or another AI

1. Open [`PORTABLE.md`](PORTABLE.md) and copy the text inside its `text` block.
2. Paste it into your AI's custom instructions, project instructions, or equivalent field.
3. Start a fresh conversation and type `lfg` followed by your rough idea.

For ChatGPT, you can use **Settings → Personalization → Custom Instructions**, or add it to a project's instructions if you only want it in that project. See [ChatGPT custom instructions](https://help.openai.com/en/articles/8096356-custom-instructions-for-chatgpt) and [ChatGPT projects](https://help.openai.com/en/articles/10169521-projects-in-chatgpt).

## Quick test

Send: `lfg help me plan a 3-day trip to Kyoto on a modest budget`

You should get a **draft prompt**, with any assumptions stated, and a request for approval. The assistant should plan the trip only after you reply `ok`. If it starts planning immediately, check that the skill or portable instructions are active in that conversation.

## License

Apache-2.0. See [`LICENSE`](LICENSE).
