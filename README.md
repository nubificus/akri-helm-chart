To update the repo :

First:

```
`git clone git@github.com:nubificus/akri.git`
`git checkout gh-pages`
```

Update the `Chart.yaml` fields  with the new Version-tag

```
type: application

version: 0.12.55 #(Change this)

appVersion: 0.12.55 #(Change this)
```

Then run  in `akri/deployments/helm the following` commands

```
helm package .

helm repo index ./ 
```

This will produce the `.tgz` file and the index.yaml.
>**_Note_**: Make sure you have deleted any previous artifacts  before re-running the 
process.

The Chart, the index.yaml and the .tgz  must be pushed in the `gh-pages` branch.

To update the repo : `helm repo update`
