# Dataset Release License Policy (v2026.4)

Every artifact published on the model hub must carry a verified effective license.

## 1. Contributing components

For each released artifact, enumerate every component that contributes content:

- the upstream dataset (always);
- the synthesis model (only for derived artifacts, i.e. artifacts whose provenance
  declares a `synthesis_model`).

Look up the license identifier reported by the model hub for each component and use
it verbatim, lowercased.

## 2. Component classification

- PERMISSIVE: `mit`, `apache-2.0`, `bsd-2-clause`, `bsd-3-clause`, `odc-by`
- RESTRICTED: any `cc-by-nc-*`, `cc-by-sa-*`, `gpl-*`, `agpl-*` or `lgpl-*`
- LEGAL_REVIEW: every other identifier, including `other`, `unknown`, or a missing
  identifier.

## 3. Artifact classification

An artifact takes the strictest classification among its components, ordered
APPROVED (all components permissive) < LEGAL_REVIEW (any component custom) <
RESTRICTED (any component non-commercial or share-alike).

## 4. Effective license

- Raw artifact (no synthesis model): the upstream dataset's license identifier.
- Derived artifact classified APPROVED: the upstream dataset's license identifier.
- Derived artifact classified LEGAL_REVIEW or RESTRICTED: `PENDING LEGAL REVIEW`.

## 5. Required follow-up

- If every artifact is APPROVED: reply on the license request issue with the full
  license summary and close the request issue.
- If any artifact is LEGAL_REVIEW or RESTRICTED: reply on the license request issue
  with the full summary and open a new tracking issue titled
  `Legal review required: <comma-separated affected artifact ids>`, describing the
  blocked components. Leave the request issue open.

In both cases, commit `compliance/license_audit.json` and update the `## License`
section of every dataset card in this repository.
