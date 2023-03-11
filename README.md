# Exercism Haskell

 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview
A Devcontainer project for the [Exercism Haskell track](https://exercism.org/tracks/haskell). It defines a Devcontainer with the Exercism client and Haskell's GHCup installer installed.

The project is designed to allows one to work through the Exercism Haskell track exercises using the Visual Studio Code editor and the Devcontainer running in a local Docker instance, a remote Docker instance or in a GitHub Codespaces environment.

The project expects that your Exercism files will be in a `haskell` subfolder.

## Requirements
It is expected:
- You are familiar with VS Code
- VS Code's Remote extensions that allows *VS Code* to use a *Container* as a development environment.
- You have an Exercism account.

### Local development
- Container Engine
  - Windows: Docker Desktop 2.0+ on Windows 10/11 Pro/Enterprise.
  - macOS: Docker Desktop 2.0+
  - Linux: Docker CE/EE 18.06+ and Docker Compose 1.21+.
- Visual Studio Code
- Git

### Remote development
- Container Engine
  - Linux: Docker CE/EE 18.06+ and Docker Compose 1.21+.
- 2 GB RAM and a 2-core CPU is recommended.

### GitHub Codepsaces
- You can use the Codespace remotely via the Browser VSCode editor and have no requirements.

## Use
- Clone this repository.
- Open the repository in Visual Studio Code.
- Reopen in Container. (`Dev Containers: Reopen in Container`)
- Open a terminal inside the container. (`View: Toggle Terminal` <kbd>Ctrl</kbd>+<kbd>`</kbd>)
- Configure the exercism cli with your token and set the workspace folder to the root folder of this project.
  ```sh
  $ exercism configure -t <your token> -w "$PWD"
  ```
- Use the exercism cli to download the exercise to work on from the haskell track.
  ```sh
  $ exercism download -t haskell -e hello-world
  ```
- Edit the provided exercise file until the provided tests pass.
- Submit your solved exercise.
  ```sh
  $ exercism submit src/HelloWorld.hs
  ```


## Related Projects
- [Exercism Haskell Track](https://exercism.org/tracks/haskell)
- [Visual Studio Code Developing inside a Container](https://code.visualstudio.com/docs/devcontainers/containers)
- [GHCup installer](https://www.haskell.org/ghcup/)
- [Devcontainers](https://containers.dev/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Docker Engine](https://docs.docker.com/engine/)
- [GitHub Codespaces](https://docs.github.com/en/codespaces)
