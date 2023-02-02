# Current Behavior
- A PR will be created for the root Helm packge in `fleet.yaml` but additional PRs will be created for each item under `targetCustomization` even though `helm.version` is not specified for each `targetCustomization`.

# Desired Behavior
- A PR should only be created for the root `fleet.yaml` file if a version is not specified under `targetCustomization[].helm.version` as the the behavior for Fleet is to take the defined default version defined at the higher level.
