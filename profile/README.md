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

- **Observe first.** Every host starts in an observe-only trial. Its packet path can only pass traffic, so nothing changes until you decide it should.
- **Earned autonomy.** Enforcement is turned up per host through the Autonomy Dial. Every decision, enforced or not, is written to a counterfactual ledger, and every action has one-click undo.
- **Explained detections.** Incidents come with a storyline and MITRE ATT&CK mapping, not just a score.
- **Evidence, not screenshots.** Signed compliance packs for SOC 2, PCI DSS v4.0, HIPAA, ISO 27001, NIST CSF 2.0 and more, verifiable offline by your auditor.

## Public repositories

The product is developed in a private repository. These public repositories are
published from it:

| Repository | What it is | Licence |
|---|---|---|
| [prosentriq-sdk-python](https://github.com/PROSENTRIQ/prosentriq-sdk-python) | Python Sensor SDK and the open event schema: build your own sensor | Apache-2.0 |
| [helm-charts](https://github.com/PROSENTRIQ/helm-charts) | Helm chart for the Kubernetes sensor (`prosentriq-agent`) | See the repository |
| [releases](https://github.com/PROSENTRIQ/releases) | Signed release artifacts and how to verify them | — |

The control plane, console and sensor engine are proprietary and offered under
the Prosentriq commercial licence.

## Pricing

| Plan | Price | |
|---|---|---|
| Trial | $0 | Observe-only, no time limit, up to 3 hosts |
| Pro | $49 per enforcing node per month | $490 per node billed yearly; every feature |
| Managed service providers | 35% off | Wholesale on every customer node, cross-customer fleet view, white-label branding |

## Contact

- Sales: sales@prosentriq.com
- Support: support@prosentriq.com
- Security: security@prosentriq.com. See our [security policy](https://github.com/PROSENTRIQ/.github/blob/main/SECURITY.md); please don't report vulnerabilities in public issues.

[prosentriq.com](https://prosentriq.com)
