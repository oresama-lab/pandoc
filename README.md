# pandoc

This repository contains a docx-style template that you can refer to when converting from markdown to docx using pandoc.

## Premise

- You need docker infrastructure. If you don't have it [see the document of docker](https://docs.docker.com/get-docker/) and create docker infrastracture on your own machine.
- We use official pandoc's docker image (pandoc/latex). Pull the image from [DockerHub](https://hub.docker.com/r/pandoc/latex/).

*Docker Pull Command is*

```
docker pull pandoc/latex
```

## Usage

The following docker run command can be used to convert markdown to a custom-styled docx file.

```bash
docker run --rm --volume "`pwd`:/data" --user `id -u`:`id -g` pandoc/latex reference.md --reference-doc=custom-reference.docx -o output.docx
```
