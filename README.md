# LaTeX Template

![latex](https://img.shields.io/badge/LaTeX-forestgreen?logo=latex&logoColor=white)
![docker](https://img.shields.io/badge/Docker-dodgerblue?logo=docker&logoColor=white)
![devcontainer](https://img.shields.io/badge/DevContainer-royalblue?logo=developmentcontainers&logoColor=white)
![gpl](https://img.shields.io/badge/License-GPLv3-crimson)
![uclm](https://img.shields.io/badge/University-UCLM-firebrick)

A LaTeX template for documenting university projects.

This template uses **LaTeX 2025** from this [Docker image](https://hub.docker.com/r/texlive/texlive) for all options.

## Docker

This template includes a *Docker Compose* configuration that creates a container based on *TexLive* image with all packages.

The project is mounted into the container in a volume at `\latex-template`, allowing to compile the project and generate a **.pdf** file at `out` directory with this command:

```bash
latexmk -pdf tex/main.tex
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
#   Compiles project in a temporary container
docker compose run --rm latex-template
```

## DevContainer

> [!WARNING]
> Only recommended if you're using **VS Code** or a compatible editor

This template includes a *DevContainer* configuration at `.devcontainer` directory.

It provides an isolated environment based on *TexLive* image with the [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) extension and preconfigurations to simplify working with and compiling LaTeX documents more easily.

## License

This project is licensed under the **GNU General Public License v3.0**. See the [LICENSE](LICENSE) file for details.
