# couchdb-docker

## TODO

- Add instructions for running on a raspberry pi (possibly have a script)

This repo includes a docker-compose file that sets up a basic couchdb instance with a CORs-enabled configuration.

This is made specifically to be the database server for [Notes](https://github.com/ste163/notes).

To run `docker-compose.yaml`:

```bash
docker-compose up -d
```

This will setup the container and the admin user and password (located in `docker-compose.yaml`).

To interact with the CouchDB server and database GUI while running the container, go to: `http://localhost:5984/_utils/`.
