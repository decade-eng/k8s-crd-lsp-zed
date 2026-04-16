# k8s-crd-lsp-zed

Zed extension that runs [k8s-crd-lsp](https://github.com/decade-eng/k8s-crd-lsp) — an LSP server providing schema-aware completions and validation for Kubernetes YAML files.

## What it provides

- Completions for `kind`, `apiVersion`, field names, and enum values
- Inline diagnostics for schema violations
- Covers built-in K8s resources and any CRDs installed in your cluster

## Installation

The extension is not yet published to the Zed extension registry. Install as a dev extension:

1. Clone this repo
2. In Zed: `Extensions` → `Install Dev Extension` → select the cloned directory

## Requirements

- `kubectl` on `PATH`
- A valid `kubeconfig` pointing at a reachable cluster
- Kubernetes 1.27+

## How it works

On first use, the extension downloads the `k8s-crd-lsp` binary from [GitHub Releases](https://github.com/decade-eng/k8s-crd-lsp/releases) and caches it locally. If `k8s-crd-lsp` is already on your `PATH`, that binary is used instead.

Supported platforms: macOS (arm64, amd64), Linux (arm64, amd64).
