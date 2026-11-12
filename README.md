# parity-report

The public site of [BabelFHIR-TS](https://www.npmjs.com/package/babelfhir-ts), served at https://babelfhir-ts.github.io/parity-report/.

| Path | Content |
| --- | --- |
| `/` | Parity report for the releases on npmjs, with its data, history and badges |
| `/docs/` | Documentation |
| `/internal/` | Maintainer report, encrypted |

The rendered site is not stored in this repository. Each part is built by the BabelFHIR-TS pipelines and attached to the [`site` release](../../releases/tag/site) as `<part>.tar.gz`, which replaces the previous build of that part. [Deploy site](.github/workflows/deploy.yml) then assembles the parts and deploys them to GitHub Pages.
