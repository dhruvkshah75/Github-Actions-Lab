# GITHUB ACTIONS
The `steps` within each job of a github event can be:
- inline/local: `run`
- actions: `- uses` 

```yaml
name: example_workflow
# github event 
# since this github event is workflow_dispatch it needs to be manually triggered 
on:
  workflow-dispatch:

# this event workflow will execute on pull and push requests to the main branch 
on:
  push: 
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

```

If there are multiple jobs then they run in parallel

We can also specify a non-default shell 
```yaml
  # Job
  dummy_task_in_python:
    runs-on: ubuntu-latest
    steps:
      - run: print("This is the dummy task in python")
        shell: python
```