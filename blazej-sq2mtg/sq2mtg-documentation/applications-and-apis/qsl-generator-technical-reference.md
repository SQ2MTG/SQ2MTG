# QSL Generator — Technical Reference

## Architecture

The project is a Flask-based web application for QSL-card generation. The repository is a fork of `RobbiNespu/qsl-generator` and includes a historical Docker deployment example.

## Deployment

### Docker

The README provides a minimal Compose service using the project's container image:

```yaml
version: '3'
services:
  qslgen:
    image: "docker.pkg.github.com/classabbyamp/qsl-generator/qsl-generator:latest"
    restart: always
```

The image reference is historical; verify registry availability before relying on it.

### Native Python

The documented local path uses Python 3.8, installs `requirements.txt`, then starts Flask:

```bash
python3.8 -m pip install -r requirements.txt
flask run
```

## Source verification boundaries

The README does not specify:

* Flask route names;
* form schema;
* template structure;
* image-processing library details;
* font handling;
* persistence model;
* authentication;
* production WSGI configuration.

These should be derived from source before writing an operational deployment guide.

## License / provenance

The repository is a public fork of `RobbiNespu/qsl-generator` and is marked MIT. When redistributing modified code, retain the applicable upstream attribution and license notices.
