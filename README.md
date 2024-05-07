this is a strict template/boilerplate. therefore, every developer on team kind of follows the same rules. don't have to worry as little as possible about
differences in development methods and coding styles between people on team.

---

### (1) Engine Locking

we're going to define the fact that this project is designed to run on **yarn**

```bash
.nvmrc: lts/iron
.npmrc: engine-strict=true
package.json: "engines": {
    "node": ">=20.11.0",
    "yarn": ">=1.22.19",
    "npm": "please-use-yarn"
  },
```

### (2) Git Setup

```bash
incomplete
```

### (3) Code Formatting and Quality Tools

```bash
eslint - For best practices on coding standards
prettier - For automatic formatting of code files
```
### (4) Git Hooks
```bash
yarn add -D husky
npx husky install
npx husky add .husky/pre-commit "yarn lint"
```

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
yarn install
# then, test the project
yarn dev
# then, build the process once
yarn build
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

yarn -v
1.22.19

node -v
v20.11.0 (Iron)

npx next --version
Next.js v14.2.3

npm -v
9.6.6
