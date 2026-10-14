# Reproduction

Use Node.js 24 and pnpm 12.9.1.

```sh
git clone https://github.com/YKDZ/turbo-root-task-recursion-repro.git
cd turbo-root-task-recursion-repro
pnpm install --frozen-lockfile --ignore-scripts
pnpm exec turbo --version # 2.11.8-canary.2
pnpm run boundaries # exits 0
pnpm exec turbo run boundaries --filter=// # exits 1: recursive_turbo_invocations
pnpm run echo-turbo # exits 0
pnpm exec turbo run echo-turbo --filter=// # exits 1: recursive_turbo_invocations
```
