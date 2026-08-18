# Agent Instructions

## Repository purpose
This repository publishes `phantom-wagmi-connector`, a TypeScript connector for integrating Phantom with wagmi v1 projects.

## Layout
- `index.ts`: connector implementation and package entrypoint.
- `tsconfig.json`: TypeScript compiler configuration.
- `README.md`: installation, usage, and connector options.

## Development commands
- `yarn build`: compile the TypeScript package with `tsc` into `dist/`.

The package does not define a working automated test command; `yarn test` intentionally exits with an error.

## Contribution constraints
- Preserve compatibility with the peer dependency ranges in `package.json`, including React 17+, wagmi 1.x, and the declared viem version.
- Keep public usage and configuration examples in `README.md` aligned with connector behavior.
- Do not commit generated `dist/` output; it is excluded by `.gitignore`.
