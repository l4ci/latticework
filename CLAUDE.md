# Latticework

A collection of structured thinking and analysis frameworks packaged as model- and harness-agnostic agent skills. One skill per folder under `skills/`.

## Adding or editing a skill

When the task is to add a new skill, or to change the structure of an existing one, read [CONTRIBUTING.md](CONTRIBUTING.md) first and follow it. It defines the required files, the SKILL.md anatomy, the `description` frontmatter that controls when a skill activates, the naming of the framework and worked-example files, and the catalog entries to update in the root README. Use [swot-analysis](skills/swot-analysis/) as the reference skill.

Do not edit `.claude-plugin/plugin.json` or `marketplace.json` when adding a skill; they discover skills by folder.

## Writing

Match the plain, concrete voice of the existing README and skill files. No em dashes. Speak in actions, never in one runtime's tool names.
