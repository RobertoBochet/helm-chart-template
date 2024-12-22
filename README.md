# Helm Chart Template

```
replace $NAME with the chart name
replace $REPO with the name of the github repo
```

[![GitHub](https://img.shields.io/github/license/RobertoBochet/$REPO?style=flat-square)](https://github.com/RobertoBochet/$REPO)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/RobertoBochet/$REPO/release.yml?label=publish%20chart&style=flat-square)](https://github.com/RobertoBochet/$REPO/releases)
[![GitHub Latest Release Version](https://img.shields.io/github/v/release/RobertoBochet/$REPO?sort=semver&display_name=release&style=flat-square)](https://github.com/RobertoBochet/$REPO/releases)
[![Static Badge](https://img.shields.io/badge/-$NAME-w?style=flat-square&logo=artifacthub&logoColor=white&logoSize=18&label=Artifact%20Hub&labelColor=417598&color=2D4857)](https://artifacthub.io/packages/helm/robertobochet/$NAME)

Helm chart template based on gitea one

## Deploy

1. Add the repository to helm
   ```shell
   helm repo add robertobochet https://robertobochet.github.io/charts
   helm repo update
   ```
2. Retrieve the default values file
   ```shell
   helm show values robertobochet/$NAME > values.yaml
   ```
3. Customize the `values.yaml`
4. Install $NAME
   ```shell
   helm install $NAME robertobochet/$NAME -f values.yaml
   ```

## Parameters

## Credits

Chart is heavily based on [gitea](https://gitea.com/gitea/helm-chart) one.
They worked great, so there is no need to reinvent the wheel.
