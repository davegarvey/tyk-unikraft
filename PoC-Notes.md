### Connecting to MDCB

Configure the build to use a config file that contains the necessary MDCB connection details. For example, set the config file in the `Kraftfile` to `tyk-dataplane.conf`:

```
cmd: ["/usr/bin/tyk", "start", "--conf", "/etc/tyk-dataplane.conf"]
```

This references the config stored within this project at `rootfs/etc/tyk-dataplane.conf`.

The Docker compose file `compose.yaml` uses environment variables to define the MDCB URL and API key. Set these to the appropriate values.
