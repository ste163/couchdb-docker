# couchdb-docker

This repo includes a `docker-compose` file that sets up a basic couchdb instance with a CORs-enabled configuration. It's to be used on your LAN and uses `http` instead of `https` because of this.

This `docker-compose` is made specifically to be the database server for [Notes](https://github.com/ste163/notes).

## Setup (MacOS, Fedora Linux)

### Requirements

- Device that supports docker
- Install [docker-compose](https://github.com/docker/compose)
- `git clone` this project

### Running the container

1. In the project directory, run

```bash
docker compose up
```

2. Once the container is running, find your local IP address:
   Typically, your local IP address will be the one that starts with `192.168.*`. It's usually the first `inet` line that doesn't start with `127.0.0.1`.

```bash
ifconfig | grep inet
```

Note: this is not a static IP address for the device running the container, so this address may change.

## Connecting to the container

The admin user and password are defined in the `docker-compose.yaml`. Because the intent of this project is to run on your LAN, this is not a secure username or password.

### Database management (GUI)

To interact with the CouchDB server and database GUI while running the container, go to: `http://localhost:5984/_utils/`. Alternatively, you can use `{your IP address}:5984/_utils/`
