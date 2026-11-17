# Architecture decision records

One file per decision. Cross-cutting decisions only: naming, licensing, hosting, how products share accounts and billing.

## Rules

- A record is immutable once its status is `Accepted`.
- A decision is changed by a new record that supersedes the old one. The old record is edited only to set `Superseded by: NNNN`.
- Template: [0000-template.md](0000-template.md).

## Index

| No. | Decision | Status |
|---|---|---|
| [0001](0001-one-namespace-and-credentials-model.md) | One namespace and credentials model for every Ocalt product | Accepted |
| [0002](0002-ocaltql-single-control-layer.md) | OcaltQL is the single control layer | Accepted |
| [0003](0003-tutorial-is-the-ocaltql-spec.md) | The OcaltQL tutorial is the specification | Accepted |
| [0004](0004-machines-connect-outbound-only.md) | Connected machines connect outbound only | Accepted |
| [0005](0005-one-credential-one-job.md) | One credential, one job | Accepted |
| [0006](0006-namespace-isolation-by-separation.md) | Namespaces are isolated by separation, not filtering | Accepted |
| [0007](0007-a-query-is-one-http-request.md) | A query is one HTTP request to the runtime | Accepted |
