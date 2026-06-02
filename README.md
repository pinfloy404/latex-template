# Latex Template

![docker](https://img.shields.io/badge/Docker-dodgerblue?logo=docker&logoColor=white)
![latex](https://img.shields.io/badge/LaTeX-forestgreen?logo=latex&logoColor=white)
![gpl](https://img.shields.io/badge/License-GPLv3-blue)

A LaTeX template for documenting university projects.

## Docker

This template uses **LaTeX 2025** from this [Docker image](https://hub.docker.com/r/texlive/texlive).

To manage the container, you can use these commands:

```bash
#   Creates container
docker compose run up -d
```

```bash
#   Closes container
docker compose run down
```

```bash
#   Closes container (Removes volumes)
docker compose run down -v
```

> [!WARNING]
> This command removes all data in the container.

## License

This repository uses the [GPLv3](https://choosealicense.com/licenses/gpl-3.0/) license.
