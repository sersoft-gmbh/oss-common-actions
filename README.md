# Common Actions

A collection of common GitHub actions that are used by our OSS repositories.
These contain both reusable workflows (inside `.github/workflows`) as well as composite actions (inside various subfolders).

**IMPORTANT:** These are not meant for general public use and will change without notice!


## Usage

Both kinds of actions can be used by referencing them in a workflow file like this:

```yaml
jobs:
  some-reusable-workflow:
    uses: sersoft-gmbh/oss-common-actions/.github/workflows/some-reusable-workflow.yml@main

  some-compose-action:
    steps:
      - uses: sersoft-gmbh/oss-common-actions/path/to/action@main
```

## Maintenance

### Swift

Adding a new Swift version requires changes in the following workflows/files:

- `swift/latest-version/action.yml`
- `swift/runner-setup-versions/action.yml`

### Xcode

Adding a new Xcode version requires changes in the following workflows/files:

- `swift/runner-setup-versions/action.yml`
- `swift/xcode-destination-specifier/action.yml`
