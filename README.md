# homelab

Flux GitOps for the home Talos cluster.

- `clusters/home` — what Flux reads; points to the folders below
- `infrastructure/controllers` — installs shared cluster pieces (Cilium, cert-manager, storage)
- `infrastructure/configs` — settings for those pieces (IP pools, issuers), applied after controllers are ready
- `apps` — the apps, applied after configs are ready
