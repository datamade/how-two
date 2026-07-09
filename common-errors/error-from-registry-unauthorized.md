# GitHub Container Registry (ghcr.io) error: Unauthorized

When attempting to build an Docker image from ghcr.io, you may get an error like this:

```shell
✘ Image ghcr.io/datamade/dpd-planning-map-etl:etl-latest Error error from registry: unauthorized
```

This means you need to generate an access token: [GitHub: Generate a fine-grained access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-fine-grained-personal-access-token)

Make sure you select the correct repo owner, and just select the one repo you need access to. 

Once you send your request, GitHub may not send a notification, so send a message to whoever you need to approve access and have them look in the DataMade organization settings, somewhere like Third-party Access > Personal access tokens > Pending requests
