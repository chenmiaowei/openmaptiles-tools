# Import SQL files into PostgreSQL

This Docker image will import all SQL files in a direcotry into PostgreSQL.
It will also create all helper functions from [postgis-vt-util(https://github.com/mapbox/postgis-vt-util)] for creating
vector tiles.

## Usage

```bash
docker run --rm \
    -v $(pwd):/sql \
    -e POSTGRES_USER="osm" \
    -e POSTGRES_PASSWORD="osm" \
    -e POSTGRES_HOST="127.0.0.1" \
    -e POSTGRES_DB="osm" \
    -e POSTGRES_PORT="5432" \
    openmaptiles/import-sql
```

