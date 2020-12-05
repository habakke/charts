# unifi-poller

This is a helm chart for [unifi-poller](https://github.com/unifi-poller/unifi-poller).

## TL;DR;

```shell
$ helm repo add habakke https://habakke.github.io/charts/
$ helm install habakke/unifi-poller
```

## Installing the Chart

To install the chart with the release name `my-release`:

```console
helm install --name my-release habakke/unifi-poller
```

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
helm delete my-release --purge
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration
Read through the charts [values.yaml](https://github.com/habakke/charts/blob/master/charts/unifi-poller/values.yaml)
file. It has several commented out suggested values.
Additionally you can take a look at the common library [values.yaml](https://github.com/habakke/charts/blob/master/charts/common/values.yaml) for more (advanced) configuration options.

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example,
```console
helm install unifi-poller \
  --set env.TZ="America/New_York" \
    k8s-at-home/unifi-poller
```
Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the
chart. For example,
```console
helm install unifi-poller habakke/unifi-poller --values values.yaml 
```

```yaml
image:
  tag: ...
```

---
**NOTE**

If you get
```console
Error: rendered manifests contain a resource that already exists. Unable to continue with install: existing resource conflict: ...`
```
it may be because you uninstalled the chart with `skipuninstall` enabled, you need to manually delete the pvc or use `existingClaim`.
