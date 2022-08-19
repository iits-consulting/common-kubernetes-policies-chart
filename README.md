# Common Kubernetes Policies

This chart contains useful policies for you kubernetes cluster.

- Verify all images are signed with cosign
- Verify all images come from allowed image repositories

## Installation

```shell
export CHART_NAME=common-kubernetes-policies
export CHART_REPO_NAME=common-kubernetes-policies
helm repo add $CHART_REPO_NAME https://iits-consulting.github.io/$CHART_REPO_NAME/
helm search repo $CHART_NAME
helm install $CHART_NAME $CHART_REPO_NAME/$CHART_NAME
```

## Acceptance criteria

Any helm chart provided by iits-consulting needs to adhere to the following acceptance criteria:

- [x] The README.md has to contain a description about the chart
- [ ] Enable custom annotations in values.yaml (does not apply)
- [ ] Define common labels for better separation of concerns
- [ ] Whenever possible, sensitive information should be injected by something like
  a [mutating webhook](https://banzaicloud.com/docs/bank-vaults/mutating-webhook/) rather than be part of your chart
- [x] Use subcharts to manage dependencies whenever possible
- [x] **Document** every values.yaml variable that is meant to be adjusted
- [x] Specify a license
- [x] Provide a default .helmignore
- [ ] Have a NOTES.txt that provides information about the deployment
