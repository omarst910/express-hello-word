# Demo Repo

This repository is used for the purpose of the Demos only. The GCP Key has been removed so this pipeline wont deploy to any cluster.

If you would like to test out the CICD workflows that have been created as part of the demos, you will need to do the following:

1. Fork the repository
2. Change the all the references found in this [file](./.github/workflows/build.yaml) of the following values:
      - PPROJECT_ID
      - GKE_CLUSTER
      - GKE_ZONE
      - HELM_REPO
3. Create a Service Account key from GCP
4. Create a Github Secret from `Settings -> Secrets -> New repository secret ` with the following details:
      - Name: `GCLOUD_SERVICE_ACCOUNT_KEY`
      - Value: `cat key.json | base64 -b 0` (Base64 encoded content of the key.json)
