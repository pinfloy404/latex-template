# Latex Template

![latex](https://img.shields.io/badge/LaTeX-forestgreen?logo=latex&logoColor=white)
![docker](https://img.shields.io/badge/Docker-dodgerblue?logo=docker&logoColor=white)
![devcontainer](https://img.shields.io/badge/DevContainer-royalblue?logo=developmentcontainers&logoColor=white)
![gpl](https://img.shields.io/badge/License-GPLv3-crimson)
![uclm](https://img.shields.io/badge/University-UCLM-firebrick)

A LaTeX template for documenting university projects.

This template uses **LaTeX 2025** from this [Docker image](https://hub.docker.com/r/texlive/texlive) for all options.

## DevContainer (Recommended)

> [!WARNING]
> Only recommended if you're using **VS Code** o similar

This template uses a *DevContainer* configuration file at `.devcontainer` folder to create a separated working space with a *TexLive* image without install multiple packages.

This *DevContainer* configuration file adds [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) to facilitate the work with LaTeX.

## Docker

This template uses a *Docker Compose* file to create a *Docker* container with a *TexLive* image and all of it's packages, mounting a volume at `\latex-template` and this command to compile and generate a **.pdf** file:

```bash
latexmk -pdf latex/main.tex
```

To manage the container and compile the project, you can use these commands:

```bash
#   Creates container
docker compose up -d
```

```bash
#   Closes container
docker compose down -v
```

```bash
#   Creates container, compiles project from Docker and closes container
docker compose run --rm latex-template
```

## License

This repository uses the [GPLv3](https://choosealicense.com/licenses/gpl-3.0/) license.
