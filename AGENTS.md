# ChatGPT GitHub Project Init

This repository uses the Luna Chat Coder development protocol.

Before repository-development work:

1. Read `.agents/skills/luna-chat-coder/SKILL.md`.
2. Treat GitHub commits and PR heads as the authoritative durable source for exact repository state.
3. Use the sandbox work container as the primary development environment when available.
4. Use GitHub Actions only for a real capability, transport, or bounded execution gap.
5. Diagnose failed Actions runs from logs and failed steps before changing source or retrying.
6. Preserve exact, task-owned durable state so work can be recovered after chat or sandbox resets.

Project-specific instructions in this repository and downstream repositories take precedence over this generic routing document where they define actual technology, build, test, or deployment requirements.
