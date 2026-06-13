# LaTeX Template

![latex](https://img.shields.io/badge/LaTeX-forestgreen?logo=latex&logoColor=white)
![docker](https://img.shields.io/badge/Docker-dodgerblue?logo=docker&logoColor=white)
![devcontainer](https://img.shields.io/badge/DevContainer-royalblue?logo=developmentcontainers&logoColor=white)
![gpl](https://img.shields.io/badge/License-GPLv3-crimson)
![uclm](https://img.shields.io/badge/University-UCLM-firebrick)

A LaTeX template for documenting university projects.

> [!IMPORTANT]
> This template is intended by default for projects at **UCLM**. Replace the images in the `tex/images` directory with your own.

This template uses a customized **TeX Live 2025** from this [Docker image](https://hub.docker.com/r/texlive/texlive) for all options.

## Local

This template can be used without Docker. These are the requirements to compile the project locally:

- TeX Live 2025 or later
- Inkscape

## Docker

This template includes a Docker Compose and a Dockerfile configuration in the `.docker` directory that creates a container and a customized image based on Tex Live image with all packages and requirements described in the [Local](#local) section.

The project is mounted into the container in a volume at `latex-template`, allowing to compile the project and generate a **.pdf** file at `out` directory with this command:

```bash
latexmk -pdf -shell-escape -outdir=out tex/main.tex
```

To manage the container and compile the project, you can use these commands:

```bash
#   Creates container
docker compose -f .docker/docker-compose.yml up -d
```

```bash
#   Closes container
docker compose -f .docker/docker-compose.yml down -v
```

```bash
#   Compiles project in a temporary container
docker compose -f .docker/docker-compose.yml run --build --rm latex-template
```

## DevContainer

> [!WARNING]
> Only recommended if you're using **VS Code** or a compatible editor.

This template includes a DevContainer configuration in the `.devcontainer` directory with the requirements described in the [Local](#local) section.

It provides an isolated environment based on Tex Live image with the [LaTeX Workshop](https://github.com/James-Yu/LaTeX-Workshop) extension and preconfigurations to simplify working with and compiling LaTeX documents more easily.

## License

This project is licensed under the **GNU General Public License v3.0**. See the [LICENSE](LICENSE) file for details.
