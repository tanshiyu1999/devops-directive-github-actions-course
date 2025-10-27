Terms
- Event
- Workflow
- Job
- Stel

Step Types:
- inline / local
- non-default shell
- other repos
  - Use commit hash


Workflow Structure
- Workflow form DAG, (use `needs` to create the dependency DAG)

Triggers
- Workflow dispatch 
- Push to branch
- Create / Update PR
- Cron Schedule
- Others
- You can filter to triggers to events with specific characteristics: (! filters what not to trigger)
  - Branch names
  - Path/ files changed

Environment Variables
- Can be scoped in
  - Workflow
  - Job
  - Step

Passing Variables
- Can pass variable between steps and jobs via step and job input/ output OR environment variables (Store string in output, consume with another step)
- Intra job output -> Input
- Intra-job env var: 
  - Do not persist across environment cuz they are ran inter environment
- Inter-job output -> Input

Secrets and Variables
- Github has built in mechanism for storage of secrets and variable
  - Github Organization
  - Repository
  - Environment (e.g. staging / production)

Contexts:
- `needs`
- `steps`
- more... (see contexts.png)