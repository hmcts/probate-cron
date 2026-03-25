# Probate Cron Helm Chart

Helm chart for the Probate kubernetes cron job. It uses the [probate-back-office](https://github.com/hmcts/probate-back-office) image to execute scheduled tasks by passing the arguments: `run [taskname]` to the jar.

## Notes

- When releasing a new version of the chart, ensure the version is updated in both:
    - `Chart.yaml`
    - [cnp-flux-config](https://github.com/hmcts/cnp-flux-config)
- DO NOT USE the tag version in flux config