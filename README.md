<p align="center">
  <img height="300" src="https://evodefipay.com/img/logo_EVODeFi_Pay.svg" alt="EvoPay">
<p>
  


## Installation

To use it on the web:

```shell
npm install evopay-sdk
```

```shell
yarn add evopay-sdk
```

## Quick start

```js
import EvoPay from 'evopay-sdk';

const merchantId = 'your-merchant-id';
const apiKey = 'your-api-key';

const evoPay = new EvoPay(merchantId, apiKey);

applyStyles();

computePosition(referenceElement, floatingElement, {
  placement: 'right',
}).then(applyStyles);
```

[Visit the docs for detailed information](https://floating-ui.com/docs/computePosition).

## Development and production builds

Floating UI is published with default, development, and
production builds, using Node's support for
[export conditions](https://nodejs.org/api/packages.html#packages_conditional_exports).

- `"default"`: uses `process.env.NODE_ENV`, in which
  your bundler handles the env variable, dead code elimination,
  and minification
- `"production"`: minified with no debug logging
- `"development"`: unminified with debug logging

If you're using a bundler like webpack, Vite, or Parcel, this is
handled for you **automatically**.

If this is not handled, you must opt into one of the builds in
tools that support export conditions. This is done differently
for each tool.

## React

- [React DOM](https://floating-ui.com/docs/react-dom)
- [React Native](https://floating-ui.com/docs/react-native) (\*experimental)

## Components

Right now, Floating UI focuses on positioning floating elements, but a package
that exposes higher-level primitives for building these elements more easily is
in development.

## Contributing

This project is a monorepo written in TypeScript using npm workspaces. The
website is using Next.js SSG and Tailwind CSS for styling.

- Fork and clone the repo
- Install dependencies in root directory with `npm install`
- Build initial package dist files with `npm run build`

### Testing grounds

`npm run dev` in the root will launch the `@floating-ui/dom` development visual
tests at `http://localhost:1234`. The playground uses React to write each test
route, bundled by Parcel. When making changes to `packages/core` or
`packages/dom`, Parcel will hot reload the app and display the changes.

Each route has screenshots taken of the page by Playwright to ensure all the
functionalities work as expected; this is an easy, reliable and high-level way
of testing the code.

Below the main container are UI controls to turn on certain state and options.
Every single combination of state is tested visually via the snapshots to cover
as much as possible.

### Website

`npm -w website run dev` in the root will launch the website at
`localhost:3000`.

## License

MIT
