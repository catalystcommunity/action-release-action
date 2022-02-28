<!-- start title -->

# GitHub Action:Hello World

<!-- end title -->
<!-- start description -->

Greet someone and record the time

<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->

```yaml
- uses: swarm-io/action-javascript-action-template@undefined
  with:
    # Who to greet
    # Default: World
    who-to-greet: ""
```

<!-- end usage -->
<!-- start inputs -->

| **Input**          | **Description** | **Default** | **Required** |
| :----------------- | :-------------- | :---------: | :----------: |
| **`who-to-greet`** | Who to greet    |   `World`   |   **true**   |

<!-- end inputs -->
<!-- start outputs -->

| **Output** | **Description**         | **Default** | **Required** |
| :--------- | :---------------------- | ----------- | ------------ |
| `time`     | The time we greeted you |             |              |

<!-- end outputs -->
<!-- start examples -->

### Example usage

```yaml
name: Semantic Release
on:
  pull_request:
    types:
      - closed
    branches:
      - main
    paths:
      - action.yaml
      - index.js
      - package.json
jobs:
  semantic-release:
    if: github.event.pull_request.merged == true
    runs-on: ubuntu-latest
    steps:
      - uses: catalystsquad/action-release-action@v1
        with:
          token: ${{ secrets.AUTOMATION_PAT }}
          release-config: ${{ secrets.JS_ACTION_RELEASE_CONFIG }}
```
<!-- end examples -->
<!-- start [.github/ghdocs/examples/] -->
<!-- end [.github/ghdocs/examples/] -->
