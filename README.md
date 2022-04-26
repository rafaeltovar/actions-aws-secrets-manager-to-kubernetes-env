# Set Kubernetes Secrets Action

## Usage
```
on: [push]

jobs:
  publish:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: twonas/set-kubernetes-secrets-action@v1
        with:
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY }}
          aws-secret-access-key: ${{ secrets.AWS_ACCESS_SECRET }}
          aws-region: ${{ secrets.AWS_SM_REGION }}
          digital-ocean-token: ${{ secrets.DIGITALOCEAN_ACCESS_TOKEN }}
          aws-secret-id: prod/Organisation/Application
          kubernetes-secret-name: application-secrets
          kubernetes-cluster-id: k8s-0-00-0-do-0-ams3-0000000000000
```
