# Contributing to Nodrail

Thanks for helping. Each repository's `CONTRIBUTING.md` explains how to set it up
and check a change. In all of them:

- Open an issue first for anything large.
- Add a test with the change. Anything that can't be decided must block.
- Contributions are made under the Apache-2.0 licence, as its section 5
  describes. There is no separate agreement to sign.
- Everyone taking part follows the code of conduct.

## Names and descriptions

Every Nodrail repository squash-merges pull requests, so a pull request's
title becomes its commit on `main`. Titles follow
[Conventional Commits](https://www.conventionalcommits.org/), and a check
enforces it:

```
type(scope): summary
```

- **type:** `feat` (something users can do that they couldn't), `fix`, `perf`,
  `refactor`, `docs`, `test`, `build`, `ci`, `chore` (no change users notice),
  or `revert`. Add `!` before the colon for a breaking change:
  `feat(client)!: …`.
- **scope:** optional, lowercase, the part it touches. In nodrail-js: `engine`,
  `client`, `hook`, `packs`, `release`. In agent-plugins: `claude-code`,
  `codex`, `hook`. Anywhere: `deps`, `ci`, `docs`.
- **summary:** lowercase, imperative ("match", not "matched" or "matches"), no
  full stop, aim for 72 characters in all.

Good: `fix(engine): match secret names case-insensitively`,
`docs(client): show the MCP server example`, `chore(deps): bump zod to 4.7`.

Commits on a branch can say what you like: only the title reaches `main`.

The description follows the template: **Why** (the problem, or `Closes #123`),
**What changed**, **How it was checked** (the commands you ran and what they
showed), and **Risk and rollback**. Automated pull requests follow the same
title rule: Dependabot uses `chore(deps)`, and releases use
`chore(release): version packages`.

## Size and shape of code

Linting enforces limits so the code grows in small, named pieces:

- at most 400 lines per file and 80 per function, not counting blank lines and
  comments;
- complexity at most 15, nesting at most 4 deep, and at most 4 parameters
  (pass an object instead);
- lines at most 80 characters, by Prettier.

Tests are exempt from the size limits. When a file nears a limit, split it by
what each part does rather than raising the limit.
