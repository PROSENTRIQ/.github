<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/PROSENTRIQ/.github/main/profile/logo-lockup.svg">
    <img src="https://raw.githubusercontent.com/PROSENTRIQ/.github/main/profile/logo-lockup-light.svg" alt="Prosentriq" width="300">
  </picture>
</p>

<p align="center"><b>Autonomous host and network protection you can prove is safe before it blocks anything,<br>with audit evidence generated for you.</b></p>

Prosentriq is one control plane plus thin, replaceable sensors. The Linux
XDP/eBPF engine is the first sensor; Kubernetes, log sources, AWS and your own
sensors speak the same open event schema.

- **Observe first.** Every host starts observe-only. Its packet path can only pass traffic, so nothing changes until you decide it should.
- **Earned autonomy.** Enforcement is turned up per host through the Autonomy Dial. Every decision, enforced or not, is written to a counterfactual ledger, and every action has one-click undo.
- **Explained detections.** Incidents come with a storyline and MITRE ATT&CK mapping, not just a score.
- **Evidence, not screenshots.** Signed compliance packs for SOC 2, PCI DSS v4.0, HIPAA, ISO 27001, NIST CSF 2.0 and more, verifiable offline by your auditor.

## Public repositories

The product is developed in a private repository. These public repositories are
published from it:

| Repository | What it is | Licence |
|---|---|---|
| [docs](https://github.com/PROSENTRIQ/docs) | The full product documentation: install, console, API, integrations, compliance, self-hosting, plans | © Torcis Ltd |
| [prosentriq-sdk-python](https://github.com/PROSENTRIQ/prosentriq-sdk-python) | Python Sensor SDK and the open event schema: build your own sensor | Apache-2.0 |
| [helm-charts](https://github.com/PROSENTRIQ/helm-charts) | Helm chart for the Kubernetes sensor (`prosentriq-agent`) | See the repository |
| [releases](https://github.com/PROSENTRIQ/releases) | Signed release artifacts and how to verify them | — |

The control plane, console and sensor engine are proprietary and offered under
the Prosentriq commercial licence.

## Pricing

Per enforcing node; observe-only hosts are never billed. Current prices are
always on [prosentriq.com/pricing](https://prosentriq.com/pricing).

| Plan | Price per enforcing node | For |
|---|---|---|
| Free | $0: up to 5 observe-only hosts, no time limit, no card | Seeing what would be blocked |
| Starter | $19 per month or $228 per year, up to 25 enforcing nodes, autonomy to level 3 | Small teams; includes SSO and the SOC 2 pack |
| Pro | $49 per month or $588 per year; $39 from 100 and $29 from 1,000 nodes | Full autonomy, every integration and framework; 7-day free trial |
| Enterprise | Annual, from 100 nodes ($468 per node per year) | Self-hosting, air-gap, federation, DPA, 24/7 SLA |
| Managed service providers | 35% off Starter and Pro | Wholesale on every customer node, billed monthly; cross-customer fleet view, white-label branding |

Annual billing is twelve months' price. Details: [Plans and billing](https://github.com/PROSENTRIQ/docs/blob/main/plans-and-billing.md).

## Documentation

Start with [Getting started](https://github.com/PROSENTRIQ/docs/blob/main/getting-started.md),
or browse [PROSENTRIQ/docs](https://github.com/PROSENTRIQ/docs).

## Contact

- Sales: sales@prosentriq.com
- Support: support@prosentriq.com
- Security: security@prosentriq.com. See our [security policy](https://github.com/PROSENTRIQ/.github/blob/main/SECURITY.md); please don't report vulnerabilities in public issues.

[prosentriq.com](https://prosentriq.com)
