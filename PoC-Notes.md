Directories contain different deployments. To run them, execute the `kraft` command from root directory, and reference the compose file using its path. E.g. for the MDCB dataplane example:

```shell
kraft cloud compose up --file ./mdcb-dataplane/compose.yaml
```

Note that the instances need to be removed using the `instance rm` command, as the `compose down` command doesn't work with the file path argument. You can remove all instance using this command:

```shell
kraft cloud instance rm --all 
```

## Deployments

### MDCB Dataplane

The Docker compose file `compose.yaml` uses environment variables to define the MDCB URL and API key. Set these to the appropriate values.

```shell
kraft cloud compose up --file ./mdcb-dataplane/compose.yaml
```

### Simple OSS

Builds a Tyk definition (`simple-oss/rootfs/opt/tyk-gateway/apps/httpbin.json`) into the image, which is then available via the `/httpbin` listen path.

```shell
kraft cloud compose up --file ./simple-oss/compose.yaml
```

### Custom Image

Builds a custom image, rather than use the Unikraft default.

```shell
kraft cloud compose up --file ./custom-image/compose.yaml
```

### Default

This is the standard deployment, as per Unikraft's Tyk example, on which the other deployments are based.

```shell
kraft cloud compose up --file ./default/compose.yaml
```
