# couchdb-docker

## TODO

- Add instructions for running on a raspberry pi (possibly have a script)

This repo includes a docker-compose file that sets up a basic couchdb instance with a CORs-enabled configuration.

This is made specifically to be the database server for [Notes](https://github.com/ste163/notes).

## Running the container (todo: cleanup formatting)

- git clone the project
- docker compose -d up
- find the local port:

```bash
ifconfig | grep inent
```

- Typically, your local IP address will be the one that starts with 192.168. or 10.. It's usually the first inet line that doesn't start with 127.0.0.1.
- TODO: will need to setup a static IP address for the device running the container so that the app can store the address

## Required software

- [docker-compose](https://github.com/docker/compose)

## Running the container

To run `docker-compose.yaml`:

```bash
docker-compose up -d
```

This will setup the container and the admin user and password (located in `docker-compose.yaml`).

To interact with the CouchDB server and database GUI while running the container, go to: `http://localhost:5984/_utils/`.
