# GitHub Container Registry (ghcr.io) error: Unauthorized

When attempting to build an Docker image from ghcr.io, you may get an error like this:

```shell
✘ Image ghcr.io/datamade/dpd-planning-map-etl:etl-latest Error error from registry: unauthorized
```

This means you need to generate a personal access token: [GitHub: Generate a CLASSIC access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-fine-grained-personal-access-token)

Then, follow the linked instructions to [authenticate with GitHub packages](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-with-a-personal-access-token-classic).
