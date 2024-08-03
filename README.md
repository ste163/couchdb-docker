# couchdb-docker

This repo includes a docker-compose file that sets up a basic couchdb instance with a CORs-enabled configuration.

This is made specifically to be the database server for [Notes](https://github.com/ste163/notes).

## Requirements

- A computer that supports docker
- Install [docker-compose](https://github.com/docker/compose)

## Create certificates

(If I can do all of this with a bash command, that would be cool!)
Because this container is running a host, we need to setup HTTPS which means creating a certificate. This will allow other devices to make secure connections, even though this is all over LAN.

## Running the container

1. `git clone` the project
2. In the project directory, run

```bash
docker compose up
```

3. Once the container is running, find your local IP address:
   Typically, your local IP address will be the one that starts with `192.168.*` or `10.*`. It's usually the first `inet` line that doesn't start with `127.0.0.1`.

```bash
ifconfig | grep inet
```

Note: this is not a static IP address for the device running the container, so this address may change when the device restarts.

## Connecting to the container

The admin user and password are defined in the `docker-compose.yaml`. Because the intent of this project is to run on your LAN, this is not a secure username or password.

### Database management (GUI)

To interact with the CouchDB server and database GUI while running the container, go to: `http://localhost:5984/_utils/`.
