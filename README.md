# Exercism Haskell

 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview
A Visual Studio Code Devcontainer project that defines a Devcontainer with an Exercism client and Haskell's GHCup installer installed. The project is to be used in Visual Studio Code and the Devcontainer run in a local Docker instance, a remote Docker instance or in a GitHub code-spaces environment.

The project expects that your *Exercism* files will be in a `haskell` subfolder and ignores them. It is expected that the *Exercism* client will be used to manage the files for a given track and not stored in git.

## Requirements
It is expected:
- You are familiar with *VS Code*, it's remote extensions that allows *VS Code* to use a *Container* as a development environment.
- You have an *Exercism* account.

### Local development
- Windows: Docker Desktop 2.0+ on Windows 10/11 Pro/Enterprise.
- macOS: Docker Desktop 2.0+
- Linux: Docker CE/EE 18.06+ and Docker Compose 1.21+.
- Visual Studio Code
- Git

### Remote development
- Visual Studio Code
- 1 GB RAM is required, but at least 2 GB RAM and a 2-core CPU is recommended.

## Use
- Clone this repository.
- Open the repository in Visual Studio Code.
- Reopen in Container
- Configure the exercism cli with your token and set the workspace folder.
  ```sh
  $ exercism configure -t <your token> -w "$PWD"
  ```

## Related Projects
- [Visual Studio Code Developing inside a Container](https://code.visualstudio.com/docs/devcontainers/containers)
- [Exercism Haskell Track](https://exercism.org/tracks/haskell)
- [GHCup installer](https://www.haskell.org/ghcup/)
- [Devcontainers](https://containers.dev/)
