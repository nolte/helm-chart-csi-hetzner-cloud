# HCloud CSI Helm Chart

Simple Helm Chart for a [hetznercloud/csi-driver](https://github.com/hetznercloud/csi-driver) Deployment.

Useable for CSI Driver [v1.2.2](https://github.com/hetznercloud/csi-driver#version-matrix)


| *Parameter*                 | *Default*        | *Description*                                                                                                             |
|-----------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------|
| ```token```                 |                  | Hetzner Cloud Personal [API Token](https://docs.hetzner.cloud/#overview-getting-started)                                  |
| ```storageClass.name```     | _hcloud-volumes_ | The kubernetes [StorageClass](https://kubernetes.io/docs/concepts/storage/storage-classes/) Name.                         |
| ```storageClass.default```  | _false_          | Set the Annotation [is-default-class](https://kubernetes.io/docs/tasks/administer-cluster/change-default-storage-class/). |


## Usage

Add the Chart Repositroy from [nolte.github.io/helm-charts](https://nolte.github.io/helm-charts/).

```bash
  helm repo add nolte https://nolte.github.io/helm-charts
  helm repo update 
  helm search repo nolte/csi-hcloud
```

```bash
helm install \
  csi-hcloud \
  nolte/csi-hcloud \
  --set "token=XYZSSSSSXXXXXXXXXAAAAA"
  -n kube-system
```
