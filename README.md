# .github

Account-wide defaults for tomjseery repositories.

`.agents/repository.json` holds the defaults for every tomjseery repository, one section each. A repository overrides a section by committing that section in its own `.agents/repository.json`.

- `access` turns on the tomjseery-bot GitHub App for agents in every tomjseery repository, through the [tj-agents GitHub access gate](https://github.com/tj-agents/github#github-access-gate). A repository opts out with `"access": {"method": "human"}`. Delete this section to turn the bot off for the whole account.
- `merge` is the default merge policy: no approval, agents may merge once the required checks pass, and nobody pushes to the default branch outside a pull request. A repository's `merge` section replaces it entirely. The schema is [github-actions:merge-policy](https://github.com/tj-agents/github-actions/blob/main/.agents/github-actions/utility/merge-policy/SKILL.md), and tj-agents/github's `github:configuration` applies it.
