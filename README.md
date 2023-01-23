# Prisma + Next.js Custom Output Not Found Repro

1. `pnpm install`
2. `cd packages/database && pnpm exec prisma generate`
3. `cd ../service && pnpm exec next build`
4. `rm -fr .next/standalone/node_modules` to workaround https://github.com/vercel/next.js/issues/42651
5. `node .next/standalone/server.js`
6. Open http://localhost:3000/api/test
7. Works fine