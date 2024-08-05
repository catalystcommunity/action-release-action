<!-- start title -->

# GitHub Action:Generate Readme and Release Action

<!-- end title -->
<!-- start description -->

Generates the README based on the action.yaml, then performs a semantic release of the action, updating the v1 tag to the latest tag

<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->

```yaml
- uses: catalystcommunity/action-release-action@undefined
  with:
    # git token to use for the run
    token: ""

    # If true, this action will disable the `include administrators` setting in branch
    # protection for this branch, and re-enable it after release. Re-enabling is run
    # using always()
    # Default: false
    toggle-admins: ""

    # The release configuration to use for the release. Set this to
    # `@catalystcommunity/release-config-javascript-actions` for javascript actions
    # Default: @catalystcommunity/release-config-composite-actions
    release-config: ""

    # Branch to update the readme on
    # Default: main
    main-branch-name: ""
```

<!-- end usage -->
<!-- start inputs -->

| **Input**              | **Description**                                                                                                                                                                |                    **Default**                    | **Required** |
| :--------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-----------------------------------------------: | :----------: |
| **`token`**            | git token to use for the run                                                                                                                                                   |                                                   |   **true**   |
| **`toggle-admins`**    | If true, this action will disable the `include administrators` setting in branch protection for this branch, and re-enable it after release. Re-enabling is run using always() |                                                   |  **false**   |
| **`release-config`**   | The release configuration to use for the release. Set this to `@catalystcommunity/release-config-javascript-actions` for javascript actions                                        | `@catalystcommunity/release-config-composite-actions` |  **false**   |
| **`main-branch-name`** | Branch to update the readme on                                                                                                                                                 |                      `main`                       |  **false**   |

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
      - uses: catalystcommunity/action-release-action@v1
        with:
          token: ${{ secrets.AUTOMATION_PAT }}
          release-config: ${{ secrets.JS_ACTION_RELEASE_CONFIG }}
```

<!-- end examples -->
<!-- start [.github/ghdocs/examples/] -->
<!-- end [.github/ghdocs/examples/] -->
