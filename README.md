# @oldbros/tsconfig

**OldBros** recommended typescript configuration

## Installing

```sh
npm install --save-dev @oldbros/tsconfig
```

## Usage

Add this line to your `tsconfig.json` file:

```json
{
  "extends": "@oldbros/tsconfig"
}
```

Add check script to your `package.json` file:

```json
{
  "scripts": {
    "check": "npx tsc --project ."
  }
}
```

Run `npm run check` command to check js files with ts compiler

[**Code examples**](https://github.com/georgolden/ts-guideline)

## Features

- Support latest ECMAScript2022 language features
- Uses ECMAScript Modules
- Recommended for NodeJS v18 and higher
- No typescript experimental features

## Description

This configuration is to check JavaScript with TypeScript compiler.

### Why doesn't **OldBros** use TypeScript as a main language:

1. There is no TypeScript RFC. Nobody knows what TypeScript actually is in details.
2. TypeScript is not a JavaScript superset. It does not support all JavaScript syntax such as `await new` and many others
3. TypeScript specific features. Enums, Namespaces, Decorators, `private` keyword (there are native js private fields)

### Why **OldBros** uses TypeScript compiler for JavaScript:

1. Explicit interfaces. They are especially useful for designing libraries and applications.
2. IDE autocompletion and hints. Those are quite useful during development time.
3. More elegant than JSDoc. The problem with JSDoc - it is quite heavy compare to TypeScript types.
4. Disctinct types and interfaces declarations with `d.ts` files are sometimes useful.
