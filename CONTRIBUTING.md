# Prerequisites

- `node: 16.x`
- `pnpm: >= 7.15.0`

# Commands

- `pnpm install` - Install dependencies
- `pnpm build` - Build the project
- `pnpm format` - Apply prettier to the project, only to changed files
  - `pnpm format:check` - Check if prettier needs to be applied, check only changed files
  - `pnpm format:check:all` - Check if prettier needs to be applied. Check all files
  - `pnpm format:all` - Same as `pnpm format`, but check all files, regardless of changes
- `pnpm lint` - Run linter
- `pnpm test` - Run tests
- CI runs equivalent of `pnpm install && pnpm format:check:all && pnpm build && pnpm lint && pnpm test`.
- `pnpm factory-reset` - if you have any problems


# Releasing

We use [monorel](https://github.com/jitsu/monorel) to publish releases.  At the moment only `@jitsu/jitsu-react`, and `@jitsu/js` are published to npm. To avoid confusion, 
always release them together, even if only one of them has changes.

## Common steps

 - Check if you're logged in with `npm whoami`, if not, run `npm login`  
 - `pnpm install && pnpm format:check && pnpm build && pnpm lint && pnpm test` should succeed
 - All changes should be committed (check with `git status`). It's ok to release canary from branches!

## Canary releases

 - `pnpm release:canary` - to **dry-run** publishing
 - Same command, but with `pnpm release:canary --publish` - to **publish**.


## Stable releases

- `pnpm release --version <put a version here>` - to **dry-run** publishing
- Same command, but with `--publish` - to **publish**.



  
