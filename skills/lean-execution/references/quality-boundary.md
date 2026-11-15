# Quality boundary

Cut repeated prose, irrelevant data, and duplicate checks. Keep evidence, work, and detail required for the user's outcome.

| Never cut | Concrete case |
| --- | --- |
| Governing instructions and business rules | Read the migration policy and schema constraints before choosing a default for legacy rows. |
| Existing behavior and relevant callers | Check alternate export entry points before moving the formatter. Keep headers, ordering, and encoding stable. |
| Negative and recovery paths | Verify that another tenant is denied access and that a failed webhook retry preserves a single ledger entry. |
| Environment and authority checks | Resolve the exact production project and revision before applying a deploy. Existing access alone is insufficient authorization. |
| Material unknowns and evidence limits | Say the staging dry-run passed and rollback was untested if rollback could not execute. Keep the affected outcome pending. |
| Sensitive data protections | Use synthetic payment events and redact secrets, account identifiers, and customer data from output. |
| User-requested detail and usable artifacts | Deliver the complete requested files and tests even when a short summary would take fewer tokens. |
| Current authoritative evidence | Verify a provider contract against current official docs when behavior is version-sensitive. Record the version when material. |

Before cutting anything, ask whether omission would change correctness, safety, evidence quality, or the user's ability to use the result. Keep it if the answer is yes. If evidence conflicts, resolve the discrepancy or label it explicitly. If a check is unavailable, use a bounded alternative and report exactly what it establishes and what remains unverified.
