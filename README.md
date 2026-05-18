# amlmarketplaces/atlassian

Claude Code marketplace federating all `@amlplugins/atlassian-*` plugins.

## Install

Add to your project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "aml-atlassian": {
      "source": { "source": "github", "repo": "amlmarketplaces/atlassian" }
    }
  },
  "enabledPlugins": {
      "atlassian-bitbucket@aml-atlassian": true,
      "atlassian-confluence@aml-atlassian": true,
      "atlassian-forge@aml-atlassian": true,
      "atlassian-jira@aml-atlassian": true,
      "atlassian-jira-service-management@aml-atlassian": true
    }
}
```

Then launch Claude Code in the project. The marketplace is fetched from `amlmarketplaces/atlassian`, cached under `~/.claude/plugins/cache/aml-atlassian/`, and each enabled plugin is loaded from its `amlplugins` source repo.

## Plugins (6 total)

- `atlassian-bitbucket` — [@amlplugins/atlassian-bitbucket](https://github.com/amlplugins/atlassian-bitbucket)
- `atlassian-confluence` — [@amlplugins/atlassian-confluence](https://github.com/amlplugins/atlassian-confluence)
- `atlassian-forge` — [@amlplugins/atlassian-forge](https://github.com/amlplugins/atlassian-forge)
- `atlassian-jira` — [@amlplugins/atlassian-jira](https://github.com/amlplugins/atlassian-jira)
- `atlassian-jira-service-management` — [@amlplugins/atlassian-jira-service-management](https://github.com/amlplugins/atlassian-jira-service-management)
- `atlassian-trello` — [@amlplugins/atlassian-trello](https://github.com/amlplugins/atlassian-trello)

## Related

- npm packages: `@amlplugins/atlassian-*` published to GitHub Packages (`https://npm.pkg.github.com`).
- Aggregating parent: [`amlmarketplaces/aml`](https://github.com/amlmarketplaces/aml) — federates every `@amlplugins/*` plugin under a single marketplace.
- AML topology: see `.claude/rules/definitions/ageni.md` § "GitHub Topology" — this repository is a Tier-4 HUB-INSTANCE under the `amlmarketplaces/` Tier-3 HUB-ORGANIZATION.

> Built by `.claude/skills/aml/metateam/marketplace/test/cross-org-amlmarketplaces-batch.mjs`.
