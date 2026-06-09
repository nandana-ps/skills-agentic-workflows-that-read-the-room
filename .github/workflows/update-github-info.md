---
name: update-github-info
description: Draft website updates for Mona's GitHub Info site from official GitHub sources.
on:
  workflow_dispatch:
  schedule:
    - cron: '17 9 * * *'
safe-outputs:
  create-pull-request:
    title-prefix: "Create Mona website updater workflow"
    draft: true
    fallback-as-issue: false
tools:
  edit:
  web-fetch:
network:
  allowed:
    - github.com
    - github.blog
    - awesome-copilot.github.com
---

# Update Mona's GitHub Info website

Read `notes/mona-notes.md` before making changes.

Use these sources:
- `notes/mona-notes.md`
- GitHub Blog: https://github.blog/latest/
- GitHub Changelog: https://github.blog/changelog/
- Awesome Copilot workflows: https://awesome-copilot.github.com/workflows/

Update `site/content/github-info.md` with concise, practical updates for readers and include source context when content comes from the GitHub Blog or GitHub Changelog.

Use the `edit` tool to update files in this repository and `web-fetch` to read the GitHub Blog, GitHub Changelog, and the Awesome Copilot workflows page.

Open a pull request for Mona to review using `safe-outputs` with `create-pull-request`.
Do not write directly to `main`.
Prefer a pull request title that mentions Mona or GitHub Info.
Check that the workflow configuration syntax is valid before finishing.