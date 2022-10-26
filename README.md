# Minimum Reproduction Repository

This repository reproduces a bug which currently occurs when using Vite in a Yarn repository using Yarn workspaces.

I have been able

## Steps

- mkdir [REPO_NAME]
- cd [REPO_NAME]
- yarn init -2
- Add the following to package.json
  ```json
  {
    "workspaces": [
      "packages/*"
    ]
  }
  ```
- cd packages
- yarn create vite vite-project --template react-ts
- cd vite-project
- yarn
- yarn dev

## Note

Strangely running `yarn create vite` creates a top-level `node_modules` directory even though the repository is using pnp.