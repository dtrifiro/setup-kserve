# Setup kserve GitHub Action

A GitHub Action to set up [kserve](https://github.com/kserve/kserve)

## Usage

```yaml
jobs:
  testing:
    runs-on: ubuntu-latest

    steps:
      - uses: dtrifiro/setup-kserve@0.0.2
        with:
          namespace: "testing-kserve"
      - name: Get all kserve namespace resources
        run: |
          kubectl get all -n "testing-kserve"
```

## Inputs

```yaml
cluster_name:
  description: "Name of the kind cluster to be created"
  required: false
  default: "kserve-testing"
namespace:
  description: "Name of the k8s namespace to create and default to"
  required: false
  default: testing
kserve_version:
  description: "kserve version (git tag) to be installed on the kind cluster"
  required: false
  default: v0.11.1.1
kserve_repo:
  description: "kserve repository to use to install kserve"
  required: false
  default: opendatahub-io/kserve
```
