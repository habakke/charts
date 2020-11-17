# hmq: High Performance MQTT Broker

This is a helm chart for [hmq](https://github.com/habakke/hmq)

## TL;DR;

```shell
$ helm repo add habakke https://habakke.github.io/charts/
$ helm install habakke/hmq
```

## Installing the Chart

To install the chart with the release name `my-release`:

```console
helm install --name my-release habakke/hmq
```

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
helm delete my-release --purge
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

Read through the [values.yaml](https://github.com/habakke/charts/blob/master/charts/hmq/values.yaml) file. It has several commented out suggested values.

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example,

```console
helm install --name my-release \
  --set config.mqtt.server="mqtt://mymqttbroker" \
    habakke/hmq
```

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart. For example,

```console
helm install --name my-release -f values.yaml habakke/hmq
```
