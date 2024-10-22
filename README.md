<img src="https://raw.githubusercontent.com/versioneer-tech/package-r-design/main/logo.png" height="15"/>

# packageR Docs

## Development

### Environment setup

Python 3.11 required.

Setup the environment:

```bash
python -mvenv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Install the [pre-commit](https://pre-commit.com/) hooks:

```bash
pre-commit install --install-hooks
```

### Serve

Edit the docs and update it live with MkDocs:

```bash
mkdocs serve
```

## Production

### Local build

Build the docs with:

```bash
mkdocs build
```

### Docker image

Build the image with:

```bash
docker build . -t package-r-docs --build-arg VERSION=$(git rev-parse --short HEAD)
```

Run it locally with:

```bash
docker run --rm -p 5000:80 --name package-r-docs package-r-docs:latest
```

## License

[CC BY-NC-SA](LICENSE) (Attribution-NonCommercial-ShareAlike) from https://creativecommons.org/licenses/by-nc-sa/4.0/