# gha-setup-java

Composite action: JDK (temurin by default) + Maven dependency caching.

```yaml
- uses: alderichoarau/gha-setup-java@v1
  with:
    java-version: "21"
    distribution: temurin
```

## Inputs

| Name | Required | Default | Description |
|---|---|---|---|
| `java-version` | No | `21` | JDK version to install |
| `distribution` | No | `temurin` | JDK distribution (`actions/setup-java`'s `distribution` input) |

## Versioning

Tags are bare `vN`, immutable, never moved -- native Dependabot `github-actions` updates work.
Release a new version: run **"Tag a new version"** (manual dispatch) -- only after an actual
change to this repo's content. Running it again with nothing new since the last tag is refused
by the workflow (it would just create a duplicate tag pointing at the same commit).
