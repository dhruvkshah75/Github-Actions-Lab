# RUNNER TYPE in GITHUB WORKFLOW 
We have different runner types
```yaml

  # === GITHUB HOSTED RUNNERS ===

  # example of runners: different OS
  runs-on: ubuntu-latest
  runs-on: windows-2022
  runs-on: macos-14 

  # running inside a container
  runs-on: ubuntu-24.04
  container: 
    image: alpine3.20

  # running using a larger VM 
  runs-on: 
    group: ubuntu-runners
    labels: ubuntu-24.04-16core



  # === 3RD PARTY HOSTED RUNNERS ===
  runs-on: namespace-profile-default
  runs-on: namespace-profile-defualt-arm64
  runs-on: namespace-profile-custom-image


  # === SELF HOSTED RUNNERS ===
  runs-on: my-self-hosted-runners-name

```