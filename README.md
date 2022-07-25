# wally-registry-builder

Builds common targets of wally's registry, so you don't have too.

# Motivation

Currently, to run a private index, you have to build the entire registry from scratch.
This can be time-consuming, and on low-RAM machines can fail outright.

# Usage

This project aims to solve this issue by building the registry for common targets automatically.

Simply download the release you need from [the releases](https://github.com/ThatTimothy/wally-registry-builder/releases).

# FAQ

<details>

<summary>How often are newer versions checked?</summary>

Every 15 minutes, but may vary based on GitHub's Action Runners' availability

</details>

<details>

<summary>How is a "new version" determined?</summary>

Whenever a new commit is issued. Since the versioning is for the CLI only, we have to check commits as well.

</details>
