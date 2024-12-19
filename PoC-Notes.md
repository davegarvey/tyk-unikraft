Directories contain different deployments. To run them, execute the `kraft` command from root directory, and reference the compose file using its path. E.g. for the MDCB dataplane example:

```shell
kraft cloud compose up --file ./mdcb-dataplane/compose.yaml
```

### Connecting to MDCB

The Docker compose file `compose.yaml` uses environment variables to define the MDCB URL and API key. Set these to the appropriate values.



