# Container Observability

## Checkpoint 4 - Application Logging

172.17.0.1 - - [08/Oct/2026:12:00:00 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"

**Explanation:** Application logs are vital for troubleshooting because they record exactly what happened and when, such as this 404 showing a visitor requested a page that doesn't exist. Without them, we would have no way to trace the cause of failures or spot suspicious requests like attempts to reach hidden admin pages.
how to add this

## Checkpoint 5 - Real-Time Container Metrics

At the time of my screenshot, the **client-website** container was using:

- **Memory Usage:** 2.738MiB
- **CPU Percentage:** 0.00%
