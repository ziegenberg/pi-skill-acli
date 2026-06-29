# pi-skill-acli

A [pi](https://pi.dev) skill for interacting with Atlassian Cloud (Jira & Confluence) via the
[acli](https://developer.atlassian.com/cloud/acli/) CLI.

Covers Jira work items (JQL search, create, edit, transition, comment, link, clone), projects,
sprints, boards, filters, and Confluence pages, spaces, and blog posts.

## Prerequisites

- `acli` must be installed (`acli --version`) and authenticated
  - OAuth: `acli auth login` (Jira + Confluence) or `acli jira auth login --web`
  - API token: `acli jira auth login --site <site>.atlassian.net --email <you> --token`
  - Verify with `acli auth status`

## Install

```bash
pi install npm:pi-skill-acli
```

## What's Included

The skill teaches the agent how to:

- **Work Items** — JQL search, view, create (incl. bulk), edit, transition, assign, clone, delete, archive
- **Comments** — create (with `--edit-last`), list, update (incl. ADF + visibility), delete
- **Selectors** — the shared `--key` / `--jql` / `--filter` pattern used by mutating commands
- **Links, Attachments & Watchers** — create/list/delete links, list/delete attachments, list/remove watchers
- **Projects** — list, view, create, update, delete, archive, restore
- **Sprints** — view, list work items, create, update, delete
- **Boards** — search, view, list sprints/projects, create, delete
- **Filters** — list, search, view, update (and reuse via `workitem search --filter`)
- **Confluence** — spaces (list/view/create/update/archive/restore), pages (view), blog posts (list/view/create)
- **Authentication** — global and product-scoped OAuth/API-token login, status, switch, logout

## License

MIT
