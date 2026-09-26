# Mintlify documentation site

The official AAS Mintlify site is configured from the repository root. `docs.json` defines the navigation and brand settings; its page paths point to canonical user and contributor guides under `docs/`. `index.mdx` is the concise site landing page.

## Source and deployment

- Git source: `sickn33/agentic-awesome-skills`, branch `main`, repository root.
- The Mintlify GitHub App can read all repositories for the `sickn33` account. The selected repository in the Mintlify project must remain `agentic-awesome-skills`.
- Commits to the connected deployment branch publish the docs. Keep AAS `main` pull-request-only and use PR preview deployments for review.
- Keep Mintlify's “push directly to your deploy branch” option disabled. AI-assisted changes should go through a reviewable pull request.
- Update canonical Markdown in `docs/users/` or `docs/contributors/`; do not maintain a second copy in the visual editor.

## AI access and boundaries

Mintlify hosts a documentation MCP endpoint at the site's `/mcp` path for searching the published docs. This exposes documentation, not the AAS skill catalog or local project files. It is separate from the local AAS MCP, which provides offline-capable, read-only catalog discovery and agent-owned stack composition.

Do not create Mintlify admin or client credentials for public documentation search. Keep automated content-fixing or merge workflows disabled unless a maintainer deliberately configures reviewed PR output and its credit usage.

## Change checks

Review `docs.json` page paths against tracked files when navigation changes. Use Mintlify's PR preview to review rendered pages before merge. Repository source validation and protected branch checks remain required; a rendered preview does not replace content review.
