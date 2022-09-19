# dora-deployment-frequency
Calculate your deployment frequency, one of DORA's four key metrics.

>**Deployment Frequency** is how often an organization successfully releases to production

## Usage
Specify your details to the workflow of your production deployment for the primary business or service. If you have multiple workflows, specify the primary one that denotes a completion of the deployment. Optionally, you can specify the particular job in the workflow.

``` yml
on:
  workflow_call:
    inputs: 
      repo:
        description: 'Repository name'
        type: string
        required: true
        default: 'dora'
      workflowName:
        description: 'Workflow name of yaml filename'
        required: true 
        type: string
      jobname:
        description: 'Job name responsible for production deployment'
        type: string
        required: false
      numberOfDays:
        description: 'Number of days to check for deployment frequency'
        type: number
        default: 7
        required: false
```

## Sample result
<img width="717" alt="Screen Shot 2022-09-19 at 9 55 09 am" src="https://user-images.githubusercontent.com/63050478/190934651-14033808-95d9-4e10-89e7-dbf419ec2e6f.png">
