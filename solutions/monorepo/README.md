---
name: Monorepo with Turborepo
slug: monorepo-turborepo
description: Learn to implement a monorepo with a single Next.js site that has installed two local packages.
framework: Next.js
useCase: Documentation
css: Tailwind
deployUrl: https://vercel.com/new/clone?repository-url=https://github.com/vercel/examples/tree/main/solutions/monorepo&project-name=monorepo&repository-name=monorepo&root-directory=apps/app&install-command=pnpm%20install&build-command=cd%20..%2F..%20%26%26%20npx%20turbo%20run%20build%20--filter%3Dapp...&ignore-command=npx%20turbo-ignore
demoUrl: https://solutions-monorepo.vercel.sh
---

# Monorepo

This is a monorepo example with a single Next.js site ([./apps/app](./apps/app)) that has installed two local packages:

- [./packages/ui](./packages/ui): Exports UI components that use TypeScript and Tailwind CSS. It's transpiled by the Next.js app using [next-transpile-modules](https://github.com/martpie/next-transpile-modules)
- [./packages/utils](./packages/utils): Exports utility functions that use TypeScript

The monorepo is using [Turborepo](https://turborepo.org/) and [pnpm workspaces](https://pnpm.io/workspaces) to link packages together, but it can also work with [yarn workspaces](https://classic.yarnpkg.com/lang/en/docs/workspaces/) or [npm workspaces](https://docs.npmjs.com/cli/v8/using-npm/workspaces).

For more examples on monorepos check out the [official Turborepo examples](https://github.com/vercel/turborepo/tree/main/examples).

> In addition to the local packages, it's also using a external package called [`@vercel/examples-ui`](../../packages/ui) that's inside this same repository, it uses `next-transpile-modules` to transpile its UI components that use CSS Modules.

## Demo

https://solutions-monorepo.vercel.sh

## How to Use

You can choose from one of the following two methods to use this repository:

### One-Click Deploy

Deploy the example using [Vercel](https://vercel.com?utm_source=github&utm_medium=readme&utm_campaign=vercel-examples):

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/vercel/examples/tree/main/solutions/monorepo&project-name=monorepo&repository-name=monorepo&root-directory=apps/app&install-command=pnpm%20install&build-command=cd%20..%2F..%20%26%26%20npx%20turbo%20run%20build%20--filter%3Dapp...&ignore-command=npx%20turbo-ignore)

## Getting Started

Execute [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) with [npm](https://docs.npmjs.com/cli/init) or [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/) to bootstrap the example:

```bash
npx create-next-app --example https://github.com/vercel/examples/tree/main/solutions/monorepo monorepo
# or
yarn create next-app --example https://github.com/vercel/examples/tree/main/solutions/monorepo monorepo
```

Next, run `app` in development mode:

```bash
pnpm
pnpm dev

# or

yarn
yarn dev

# or

npm install
npm run dev
```

The app should be up and running at http://localhost:3000.

Deploy it to the cloud with [Vercel](https://vercel.com/new?utm_source=github&utm_medium=readme&utm_campaign=monorepo-example) ([Documentation](https://nextjs.org/docs/deployment)).
