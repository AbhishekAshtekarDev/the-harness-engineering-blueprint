# AGENTS.md

<!--
Template from The Harness Engineering Blueprint companion repository:
https://github.com/AbhishekAshtekarDev/the-harness-engineering-blueprint

How to use it:
- Keep this file close to 100 lines. Move long material into docs/ and link to it.
- Put commands first. An agent that knows the exact command for one test checks its work far more often.
- Add a line under "Known mistakes" each time an agent gets something wrong that guidance would have prevented.
- Delete lines that stopped mattering.
- Any rule that must ALWAYS hold also needs enforcement in code (a deny rule, hook, linter or sandbox limit).
  A line in this file is a request. A permission rule is a guarantee.
Delete this comment block when you are done.
-->

## Project
One or two sentences: what this project is and who uses it.

## Commands
- Install: `npm install`
- All tests: `npm test`
- One test file: `npm test -- path/to/file.test.ts`
- Lint and types: `npm run lint && npm run typecheck`
- Run locally: `npm run dev`

## Structure
- App code in `src/`, tests next to the code as `*.test.ts`
- Shared helpers in `src/lib/`
- Never edit `config/`, `migrations/` or generated files in `dist/` (ask a human)

## Conventions
- Rules a linter cannot enforce, one per line
- Example: weeks run Monday to Sunday in the user's local time zone
- Example: use the date helpers in `src/lib/dates.ts`, do not add new date libraries

## Before you finish
- Run lint, typecheck and the tests for every file you changed
- Do not claim success until those checks pass
- List any assumptions in the pull request description

## Known mistakes
- One plain line per mistake an agent has made in this project before

## More detail
- Architecture: `docs/architecture.md`
- Testing guide: `docs/testing.md`
