# Eslint prettier config

## Introduction

Hi! This is my variant of eslint & prettier configuration for
fullstack development (or just for frontend / backend) with these techonologies: TypeScript + React + Node. Thanks for author of [this guide](https://blog.logrocket.com/reduce-effort-shared-eslint-prettier-configs/), which really helped me to set this config.

## Installation

First of all install packages like dev deps, which contains configuration files

```
yarn add -D @tcaty/eslint-config @tcaty/prettier-config
```

Next step is peer-deps installation. If you haven't installed peer deps before, execute command below. This one will install cli which provides peer deps installation.

```
yarn global add install-peerdeps
```

Install peer deps

```
install-peerdeps -D @tcaty/eslint-config
install-peerdeps -D @tcaty/prettier-config
```

After these steps your dev deps in `package.json` should looks like this

```
"devDependencies": {
  "@tcaty/eslint-config": "1.0.3",
  "@tcaty/prettier-config": "1.0.3",
  "eslint": "^8.15.0",
  "prettier": "^2.6.2",
  ...otherPeerDeps,
  ...otherDeps
}
```

## Configuration

The last thing that we need to do is creating of config file, it is really simple

Create two files in the root of your project

Configure your `.eslintrc` file

```
{
  "extends": ["@tcaty/eslint-config"],
  ...hereYouCanAlsoOverrideRules
}
```

Configure your `.prettierrc` file

```
"@tcaty/prettier-config"
...hereYouCanAlsoOverrideRules
```

## Conclusion

Well, that it's all. Don't forget enable fix on save action in your IDE and provide path to `.eslintrc`. Hope this little guide was helpfull :)
