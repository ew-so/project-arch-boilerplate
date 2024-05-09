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
"lint": "next lint",
{
  "extends": ["next", "next/core-web-vitals", "eslint:recommended"],
  "globals": {
    "React": "readonly"
  },
  "rules": {
    "no-unused-vars": [
      1,
      { "args": "after-used", "argsIgnorePattern": "^_" }
      // "no-unused-vars": 0, // As example: Will never bug you about unused variables again
    ]
  }
}

prettier - For automatic formatting of code files
"prettier": "prettier --write .",
{
  "trailingComma": "es5",
  "tabWidth": 2,
  "semi": true,
  "singleQuote": true
}
```

### (4) Git Hooks

```bash
yarn add -D husky
npx husky init
echo "yarn lint && yarn prettier" > .husky/pre-commit
echo "yarn build" > .husky/pre-commit
{
  "scripts": {
-   "prepare": "husky install"
+   "prepare": "husky"
  }
}
```

### (5) Git commit lint

standard convention for all our commit messages so far, let's ensure that everyone on the team is following them as well (including ourselves!)

To configure it we will be using a set of standard defaults, but I like to include that list explicitly in a commitlint.config.js file since I sometimes forget what prefixes are available:

```bash
yarn add -D @commitlint/config-conventional @commitlint/cli
commitlint.config.js
echo 'npx --no-install commitlint --edit $1' > .husky/commit-msg
```

### (6) VS Code Configuration

```bash
.vscode/settings.json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll": true,
    "source.organizeImports": true
  }
}
```

### (7) VS Code Debugging

```bash
.vscode/launch.json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll": true,
    "source.organizeImports": true
  }
}
```

### (8) Directory Structure

```bash
.vscode/launch.json
{
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll": true,
    "source.organizeImports": true
  }
}
```

### (9) Storybook

storybook it is a kind of an all-in-one component demo suite, we can build
components and show them and test them in storybook so completely isolated from our application

that's really the key thing here so if you're working on a card if you're working on a date picker if you're working on a even just like a layout element something that like a wrapper for a form or something like that you can create those components in react here but rather than having to build and load

you build them in isolation using what's called stories which are
descriptions of props and state for how to render different versions of that component and storybook as a tool will display them with those
props and state and also let you change things like you know the break the mobile break points test responsiveness change the props uh dynamically with a little ui and controls and buttons to to
see what they look like in different states

```bash
npx storybook@latest init

```

---

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
