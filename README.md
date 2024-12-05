### kargo-demo-01: Argo CD Driven | Commit Only

In this example, stage-specific Argo CD `Application` resources track
updates from a Git repository managed by Kargo. Kargo watches a specific
branch of that repository (named `kustomize`) for new commits.

New commits are promoted through stages by updating the `targetRevision`
field of each stage's corresponding Argo CD `Application` resource, which Kargo automates.

This example uses Kustomize to manage configurations for each stage within the
same branch, `kustomize`. However, using Kustomize is optional here and doesn't
impact the core setup, as the configurations could be managed with other tools or approaches.
