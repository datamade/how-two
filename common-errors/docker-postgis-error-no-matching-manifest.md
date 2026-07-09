# Image postgis/postgis: No matching manifest for linux/arm64

```
✘ Image postgis/postgis Error no matching manifest for linux/arm64/v8 in the manifest list entries
Error response from daemon: no matching manifest for linux/arm64/v8 in the manifest list entries: no match for platform in manifest: not found
```

## The problem 

You may get this error when running `docker build` or `docker compose`.

This happens because Docker is trying to locate a postgis image matching Apple Silicon architecture (arm64) and none exists as of yet. 

If such support does come to pass, you will see updates support here: https://github.com/postgis/docker-postgis#versions-2026-06-19

Example: https://github.com/datamade/chi-block-builder/issues/437

## Solution

You need to pin postgis to amd64 in your `docker-compose.yml` file.

For example
```diff
  postgres:
     container_name: name
     image: postgis/postgis
+    platform: linux/amd64
```

Example: https://github.com/datamade/chi-block-builder/pull/438
