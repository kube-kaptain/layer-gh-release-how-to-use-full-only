# Layer GH Release How To Use Full Only

Kaptain config layer that makes the "How to Consume" section of GitHub release
notes show the fully qualified reference alone.

Projects that reference this layer inherit:

- **`consumerReferenceForms: full-only`**: the release notes show one
  reference, fully qualified (`ghcr.io/my-org/my/my-app:[1.2.3]`), with no
  label and no org-local alternative

The full form carries registry, namespace, prefix and name, so it works from any
org, registry or platform. The org-local short form is omitted because it only
resolves for projects that share this registry and namespace, which a consumer
outside the org does not.


## When to use this

Reach for this layer on public packages intended for cluster consumption but
not generic build use. These types of packages are only ever consumed by other
orgs in `product-*` products, `run-*` environments, or repackaging projects.
