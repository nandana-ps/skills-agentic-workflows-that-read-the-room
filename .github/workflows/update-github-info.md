---
name: update-github-info
description: Draft website updates for Mona's GitHub Info site from official GitHub sources.
on:
  workflow_dispatch:
safe-outputs:
  create-pull-request:
    title-prefix: "Update GitHub Info"
    draft: true
    fallback-as-issue: false
tools:
  edit:
network:
  allowed:
    - github.com
---

# Update Mona's GitHub Info website

Read `notes/mona-notes.md` before making changes.

Review the existing entries in `site/content/github-info.md` to understand the format.

Add one new, concise entry about a recent GitHub feature or update. Keep it brief (2-3 sentences) and include a source reference where applicable.

Use the `edit` tool to update `site/content/github-info.md` and open a pull request for review using `safe-outputs`.
