To update the repo :

Update the Chart with the new Version-tag and the new index.yaml
(produced by running in akri/deployments/helm the following commands)

```
helm package .
helm repo index ./ 
```
The chart and the index must be pushed in the `gh-pages` branch.

To update the repo : `helm repo update`
