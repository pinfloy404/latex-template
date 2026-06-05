# Latex Template

![latex](https://img.shields.io/badge/LaTeX-forestgreen?logo=latex&logoColor=white)
![docker](https://img.shields.io/badge/Docker-dodgerblue?logo=docker&logoColor=white)
![devcontainer](https://img.shields.io/badge/DevContainer-royalblue?logo=developmentcontainers&logoColor=white)
![gpl](https://img.shields.io/badge/License-GPLv3-crimson)
![uclm](https://img.shields.io/badge/University-UCLM-firebrick)

A LaTeX template for documenting university projects.

## DevContainer (Recommended)

This template uses **LaTeX 2025** from this [Docker image](https://hub.docker.com/r/texlive/texlive), this is intended for **VS Code**.

DevContainer configuration file adds [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) to facilitate work with LaTeX.

## Docker

This uses the same [Docker image](https://hub.docker.com/r/texlive/texlive) as before.

To manage the container and compile the project, you can use these commands:

```bash
#   Creates container
docker compose up -d
```

```bash
#   Compile project
docker compose run --rm latex-template
```

```bash
#   Closes container
docker compose down
```

```bash
#   Closes container (Removes volumes)
docker compose down -v
```

> [!WARNING]
> This command removes all data in the container.

## License

This repository uses the [GPLv3](https://choosealicense.com/licenses/gpl-3.0/) license.
