Runner Types
- Where the workflow executed is controlled with the "runs-on" field
  - Github hosted, 3rd Party hosted, Self hosted

- Runner type specified controls
  - VM image used (OS + Dependeicies)
  - Resources available (CPU + Memory)


Persisting Data (Artifacts)
- It can persist data after the ephemeral job
- can produce and consume artifact

Persisting Data (Cache)
- ALlow us to reuse data across jobs and workflow
- We have official action actions/cache
- Data stored in remote object storage (Capped at 10GB)

GitHub Token Permission
- a short lived github access token is generated for each workflow run
- Scope the permissions the workflow has with the Github API
- `GH_TOKEN`: provided by runner for authentication

External Service Auth
- Static Credential (API Key): Long live credential stored in GHA secrets
- OIDC Token: Short-live credential retrieved at run time

Matrix and Conditionals
- Matrix: Run multiple copies of job with diff config
- Conditionals (if)
- Concurrency (how multiple runs of same workflow should be handled)