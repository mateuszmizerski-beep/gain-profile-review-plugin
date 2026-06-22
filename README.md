# Gain Profile Review Plugin

Internal Claude Code plugin for reviewing analyst-drafted Gain company profiles.

## Install

Add this GitHub repository as a marketplace:

```text
/plugin marketplace add mateuszmizerski-beep/gain-profile-review-plugin
```

Install the plugin:

```text
/plugin install gain-profile-review@gain-review
```

Invoke the skill:

```text
/gain-profile-review:gain-profile-review 5052872
```

The Gain connector or MCP must be configured separately in each reviewer's Claude environment.

## Update

Refresh the marketplace and installed plugin:

```text
/plugin marketplace update gain-review
/plugin update gain-profile-review@gain-review
/reload-plugins
```

The plugin intentionally omits a fixed version. Each Git commit therefore acts as a new version.

## Maintenance

The canonical skill is located under:

```text
plugins/gain-profile-review/skills/gain-profile-review/
```

Keep `SKILL.md` and all files under `references/` together. Update expert corrections in
`references/expert-calibration.md`; update the larger handbook only when the underlying guidance
changes.
