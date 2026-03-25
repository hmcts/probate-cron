# Probate Cron Helm Chart

Helm chart for the Probate kubernetes cron job. It uses the [probate-back-office](https://github.com/hmcts/probate-back-office) image to execute scheduled tasks by passing the arguments: `run [taskname]` to the jar.

## Notes

- When releasing a new version of the chart, ensure the version is updated in both:
    - `Chart.yaml`
    - [cnp-flux-config](https://github.com/hmcts/cnp-flux-config)
- It requires to create a new tag to trigger the build on Azure pipeline. The chart is published to Azure Container Registry (ACR) under helm/probate-cron with the same version as the tag.