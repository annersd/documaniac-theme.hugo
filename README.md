# Documanic Hugo Theme

## Quick Links

- [Hugo Website](https://gohugo.io/)
- Used Theme: [Docsy](https://github.com/google/docsy)

## Prerequisites

Please ensure the following software is available on your system:

- [Go](https://go.dev/dl/)
- Hugo Extended: Install it with Chocolatey: `choco install hugo-extended`
- Node.js: Install it with Chocolatey: `choco install nodejs-lts`

## Setup

1. After installing the required software, please restart Visual Studio Code to apply PATH variable changes.
2. Install all required dependencies with:
   ```bash
   npm install
   ```

### Local Development

To build and preview the website locally, run the following command:
```bash
hugo server
```
The website will be served locally and its URL will be displayed in the terminal.

### Building a Website for Deployment

To create a website ready for deployment, use:
```bash
hugo
```
The generated output will be located in the `public` folder.

## Deployment with Docker

In addition to local development, the documentation can also be deployed with Docker. The Docker image `floryn90/hugo:ext-ubuntu` is used. This image contains all the necessary dependencies to build and serve the documentation.

To generate the documentation once with Docker, run:
```bash
docker run --rm -it -v "${PWD}:/src" -p 1313:1313 floryn90/hugo:ext-ubuntu
```

To serve the documentation locally using Docker, run:
```bash
docker run --rm -it -v "${PWD}:/src" -p 1313:1313 floryn90/hugo:ext-ubuntu server
```

Additionally, you may use the following commands:
```bash
docker run --rm -it -v "${PWD}:/src" -p 1313:1313 floryn90/hugo:ext-ubuntu shell
```

```bash
hugo server --gc --minify --disableFastRender --poll 250 --buildDrafts
```

In both cases, the results will be stored in the `public` folder.