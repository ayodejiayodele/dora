# dora-deployment-frequency
Calculate your deployment frequency, one of DORA's four key metrics.

>**Deployment Frequency** is how often an organization successfully releases to production

## Usage
Specify your details to the workflow of your production deployment for the primary business or service. If you have multiple workflows, specify the primary one that denotes a completion of the deployment. Optionally, you can specify the particular job in the workflow.

``` yml
jobs:
  # This workflow contains a single job called "build"
  get-dora:
    uses: ayodejiayodele/dora/.github/workflows/deployment-frequency.yml@main
    with:
      owner: ayodejiayodele
      repo: repotest
      workflowName: ci-cd-myapp.yml
      numberOfDays: 70
    secrets:
      githubToken: ${{ secrets.YOUR_REPO_READONLY_PAT }}
```

## Sample result
<img width="717" alt="Screen Shot 2022-09-19 at 9 55 09 am" src="https://user-images.githubusercontent.com/63050478/190934651-14033808-95d9-4e10-89e7-dbf419ec2e6f.png">
