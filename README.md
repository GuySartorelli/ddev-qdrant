# DDEV qdrant Addon

This addon sets up a qdrant instance for your DDEV project. qdrant is a vector similarity search engine and vector database.

## Installation

To install the addon in your exiting ddev project, for DDEV v1.23.5 or above run

```sh
ddev add-on get netz98/ddev-qdrant
```

For earlier versions of DDEV run

```sh
ddev get netz98/ddev-qdrant
```

Then restart your project

```sh
ddev restart
```

## Usage

After installation, you can access the qdrant instance by visiting `https://<yourname>.ddev.site:6333`.
For accessing the dashboard you can visit `https://<yourname>.ddev.site:6333/dashboard`

Run `ddev describe` to list your project's services and their URLs.

Different clients can be found  in [qdrant Github](https://github.com/qdrant/qdrant?tab=readme-ov-file#clients)

## Configuration

### qdrant Settings

Settings are in general defined in the file `.ddev/docker-compose.qdrant.yaml` via environment variables.

An overview of the possible configrations can be found here:
https://qdrant.tech/documentation/guides/configuration/#configuration

### Collections

The qdrant collections will be created as folder in  `.ddev/qdrant_data/collections`.

## Logging

qdrant logs are directed to the container's stdout. You can view the logs with `ddev logs -s qdrant`.
