# Kubewarden policy psp-flexvolume-drivers

## Description

Replacement for the Kubernetes Pod Security Policy that controls Flex Volume drivers.

## Settings

This policy allows to provide a list of allowed Flex Volume drivers.

The configuration supports a list of allowed flex volume drivers. An example follows:

```yaml
allowedFlexVolumes:
  - driver: example/lvm
  - driver: example/cifs
```

If the pod to be evaluated has a different driver on any `flexVolume` volume, it will be rejected.
