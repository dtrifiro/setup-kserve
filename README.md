# Setup kserve GitHub Action

A GitHub Action to set up [kserve](https://github.com/kserve/kserve)

## Usage

```yaml
jobs:
  testing:
    runs-on: ubuntu-latest

    steps:
      - uses: dtrifiro/setup-kserve@0.0.1
      - name: Get all kserve namespace resources
        run: |
          kubectl get all -n kserve
```
