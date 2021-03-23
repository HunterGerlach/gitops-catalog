# OpenShift GitOps Operator

Installs the OpenShift GitOps (Argo CD) operator.

Do not use the `base` directory directly, as you will need to patch the `channel` and `version` based on the version of OpenShift you are using, or the version of the operator you want to use.

The current *overlays* available are for the following channels:
* [preview](overlays/preview)

## Usage

If you have cloned the `catalog` repository, you can install the OpenShift GitOps operator based on the overlay of your choice by running from the root `catalog` directory

```
oc apply -k openshift-gitops-operator/overlays/<channel>
```

Or, without cloning:

```
oc apply -k https://github.com/redhat-canada-gitops/catalog/openshift-gitops-operator/overlays/<channel>
```