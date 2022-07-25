# wally-registry-builder

Builds common targets of [wally](https://wally.run)'s registry, so you don't have too.

# Motivation

Currently, to run a private registry, you have to build the entire registry from scratch.
This can be time-consuming, and on low-RAM machines can fail outright.

This project aims to solve this issue by building the registry for common targets automatically.

# Usage

Simply download the release you need from [the releases](https://github.com/ThatTimothy/wally-registry-builder/releases).

## Backend

To use the backend, navigate to the `wally-registry-backend` folder.

First, configure `Rocket.toml` to your liking.
Then, run the backend using the included `launch` binary.
This will be `launch.exe` for windows, and `launch` for every other platform.

## Frontend (optional)

Because the frontend relies on env variables (for the api) at runtime, the frontend is not automatically built.

To use the frontend, you will need to install [node](https://nodejs.org/).

To build the frontend, navigate to the `wally-registry-frontend` folder and run:

```bash
npm install
npm run build
```

To run the frontend, use node:

```
node build/server/server.js
```

# FAQ

<details>

<summary>How often are newer versions checked?</summary>

Every 15 minutes, but may vary based on GitHub's Action Runners' availability

</details>

<details>

<summary>How is a "new version" determined?</summary>

Whenever a new commit is issued. Since the versioning is for the CLI only, we have to check commits as well.

</details>
