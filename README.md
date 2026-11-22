# homelab

Flux GitOps for the home Talos cluster.

- `clusters/home` — what Flux reads; points to the folders below
- `infrastructure/controllers` — installs shared cluster pieces (Cilium, cert-manager, storage)
- `infrastructure/configs` — settings for those pieces (IP pools, issuers), applied after controllers are ready
- `apps/base` — each app's HelmRelease, shared by both environments
- `apps/testing` — namespace `testing`, deployed from the `development` branch
- `apps/production` — namespace `production`, deployed from the `main` branch

Flow: PR into `development` → testing; merge `development` into `main` → production.
