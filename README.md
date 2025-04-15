# Sedimark platform deployment

This repository contains manifests and instructions to deploy the Sedimark platform.

## Local deployment with Docker 

### Prerequisites

Ensure you have Docker compose installed, version 2.23.0 or higher. You can check this by running:

```bash
docker compose version
```

If you don't have Docker compose installed, you can install it by following the instructions in the [Docker documentation](https://docs.docker.com/compose/install/).

### Marketplace only

If you wish to deploy only the marketplace and its necessary dependencies, you can do so by running the following command:

```bash
cd mvm
docker compose --env-file .env up -d
```

Feel free to modify the `.env` file to suit your needs. The default configuration should work for most users.

⚠️ This Docker compose contains a catalogue instance: it is present only for testing purposes. You can point to any other remote catalogue by setting the `MARKETPLACE_CATALOGUE_URL` environment variable in the `.env` file. The catalogue instance is not meant to be used in production.

### Full deployment

If you wish to deploy the full Sedimark platform, including the marketplace and the Sedimark toolbox, you can do so by running the following command:

```bash
cd mvm_mvi
docker compose up -d
```

