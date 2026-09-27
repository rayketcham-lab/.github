# Ketcham Lab — reorganization in progress

We're consolidating our infrastructure around a central orchestration setup:

- **ubuntu3** is the orchestrator: projects live in `/opt/llm/projects/`, Grok agents work from there.
- **GitHub** remains the source of truth; target machines (ubuntu2, Rocky, AWS, Windows3090) receive code via self-hosted CI runners and deploy workflows.
- Most repositories in this org have been made **private** while the reorganization settles.

If you need access to something here, open an issue or contact the org owner.
