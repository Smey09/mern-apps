# Turborepo starter

This is an official starter Turborepo.

## Structure Projects
    ```
    mern-app/
    ├── apps/
    │   ├── dashboard/    (Next.js for admin interface)
    │   ├── client/       (Next.js for user interface)
    │   └── express-api/  (Express API for back-end)
    ├── package.json      (Monorepo config using npm workspaces)
    └── tsconfig.json     (Optional: shared TypeScript config)
    ```
## how to setup
    - Create Mern-app/
        - ```npx create-turbo@latest ```
    - Create dashboard/
        - cd apps/
        - npx create-next-app@latest dashboard
            ``` ✔ Would you like to use TypeScript? … No / Yes
                ✔ Would you like to use ESLint? … No / Yes
                ✔ Would you like to use Tailwind CSS? … No / Yes
                ✔ Would you like to use `src/` directory? … No / Yes
                ✔ Would you like to use App Router? (recommended) … No / Yes
                ✔ Would you like to customize the default import alias (@/*)? … No / Yes
                ✔ What import alias would you like configured? … @/*```
            - cd dashboard
            - touch tsconfig.json
            - npm install --save-dev typescript @types/react @types/node
    - Create client/
        - cd ../
        - npx create-next-app@latest client
            ``` ✔ Would you like to use TypeScript? … No / Yes
                ✔ Would you like to use ESLint? … No / Yes
                ✔ Would you like to use Tailwind CSS? … No / Yes
                ✔ Would you like to use `src/` directory? … No / Yes
                ✔ Would you like to use App Router? (recommended) … No / Yes
                ✔ Would you like to customize the default import alias (@/*)? … No / Yes
                ✔ What import alias would you like configured? … @/*```
           - cd client
           - touch tsconfig.json
           - npm install --save-dev typescript @types/react @types/node
    - Create express-api/
        - cd ../
        - mkdir express-api
        - cd express-api
            - npm init -y
            - npm install express

## Using this example

Run the following command:

```sh
npx create-turbo@latest
```

## What's inside?

This Turborepo includes the following packages/apps:

### Apps and Packages

- `docs`: a [Next.js](https://nextjs.org/) app
- `web`: another [Next.js](https://nextjs.org/) app
- `@repo/ui`: a stub React component library shared by both `web` and `docs` applications
- `@repo/eslint-config`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `@repo/typescript-config`: `tsconfig.json`s used throughout the monorepo

Each package/app is 100% [TypeScript](https://www.typescriptlang.org/).

### Build

To build all apps and packages, run the following command:

```
cd my-turborepo
pnpm build
```

### Develop

To develop all apps and packages, run the following command:

```
cd my-turborepo
pnpm dev
```

### Remote Caching

Turborepo can use a technique known as [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```
cd my-turborepo
npx turbo login
```

```
npx turbo link
```
