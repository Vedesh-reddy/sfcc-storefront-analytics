# Contributing

Start from `main` and create a focused `feature/`, `fix/`, or `docs/` branch. Keep behavior changes and documentation accurate together.

```sh
npm ci
npm run validate
npm run package:metadata
```

CI mocks cannot check platform quotas, real browser beacons, order post-processing (invoices), Business Manager permissions or metadata installation. For a platform behavior change, exercise the affected feature on a sandbox, following the sandbox verification plan in [docs/analytics-testing.md](docs/analytics-testing.md). In the PR, say which checks were automated and which were manual.

Preserve these rules:

- browser events never carry money: cart, checkout and purchase figures come from the server and from orders;
- a storefront request creates at most one custom object and never updates an aggregate; only the job steps write aggregates, under the writer lock;
- an order contributes the difference to its stored snapshot, so every reconciliation can be repeated without counting twice;
- a custom object query uses at most 4 custom attribute expressions, and session state stays under the 2000-character limit (the tests enforce both);
- every Business Manager page is a permission-scoped menu action; parameters are allow-listed or pattern-checked.

Keep credentials and generated output out of Git. Add new attributes to the metadata and to [docs/analytics-data-model.md](docs/analytics-data-model.md), and new labels to the `analyticsadmin` resource bundle.

See [NOTICE.md](NOTICE.md) for attribution and terms.
