# actions-aws-secrets-manager-to-kubernetes-env

## Usage
```
on: [push]

jobs:
  publish:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: rafaeltovar/actions-aws-secrets-manager-to-kubernetes-env@v1
        with:
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY }}
          aws-secret-access-key: ${{ secrets.AWS_ACCESS_SECRET }}
          aws-region: ${{ secrets.AWS_SM_REGION }}
          aws-secret-id: prod/Organisation/Application
          kubernetes-secret-name: application-secrets
```
