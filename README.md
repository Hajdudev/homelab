# homelab

Flux GitOps for the home Talos cluster.

- `clusters/home` — what Flux reads; points to the folders below
- `infrastructure` — shared cluster pieces (ingress, storage, certs)
- `apps` — the apps, applied after infrastructure is ready
