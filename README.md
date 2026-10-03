# UCE Evidence Lens for Gemini

**Public preview · 0.1.0-preview.1**

Inspect public UCE records in Gemini and understand what the evidence supports.
UCE Evidence Lens separates integrity checks, transaction chronology, recorded
assertions, and coverage limits. You can also request a fresh, unsigned inspection
report for an explicit public record.

[Overview and setup](https://uceevidencelens.com/gemini/)
· [Download the Gemini skill](https://github.com/hedward/uce-evidence-lens-gemini/releases/download/v0.1.0-preview.1/inspect-uce-evidence.zip)
· [Setup guide](INSTALL.md)
· [Preview status](CHANGELOG.md)
· [Support](SUPPORT.md)

## Get started

You need access to Gemini's custom connected apps and skills. Our tested workflow
uses **Gemini Spark on the web**. Google controls account, region, subscription,
and rollout eligibility; check access before downloading.

1. Add this custom app in Gemini's **Settings → Connected Apps** (sometimes under
   **Personal Intelligence**):

   ```text
   https://uce-evidence-lens-claude-zptt2ggs7a-uc.a.run.app/mcp
   ```

2. Download `inspect-uce-evidence.zip`, then upload it in **Settings → Skills**.
3. In Spark, select **UCE Evidence Lens** with `@` and **inspect-uce-evidence**
   with `/`. Supply a public record reference and ask for inspection.

Connecting the app and uploading the skill are separate steps. No UCE account,
API key, original-file upload, payment, or local software installation is needed.
Gemini access may require a Google subscription. The full walkthrough and example
prompts are in [INSTALL.md](INSTALL.md).

## What you can do

| Tool | Result |
| --- | --- |
| `inspect_uce_record` | Separate format, covered manifest-hash, platform-signature, chronology, assertion, and coverage results. |
| `get_uce_inspection_report` | A fresh unsigned, dated JSON snapshot bound to the public record you identify. |

Checks run on the UCE server using the reviewed Lens verifier. The skill helps
Gemini interpret the returned results; it is not a verifier on its own.

**Integrity checks do not establish identity, authorship, ownership, rights,
consent, or a creation date. An unsigned inspection report is not a UCE Certificate
or a new permanent record.** No accounts, original-work uploads, evidence creation,
certificate issuance, payments, or local-file comparison are included. Use the
[Evidence Lens browser](https://uceevidencelens.com/) for local-file comparison.

## Preview status

Native Gemini Spark inspection and report calls succeeded in our October 3, 2026
test, each after one retry. Spark also produced blank or failed turns, including
on a simple task that used no tools. Availability and reliability remain variable.
Native report-file downloads, corrected direct-link rendering, ordinary-chat
tool access, and mobile use are not verified for this release. Reports can be
explained in the conversation; a downloadable attachment is not promised.

This is a public **direct-install preview**. It has not been submitted to or listed
in a Google app catalog. It is independently operated and does not imply Google,
Anthropic, or OpenAI endorsement. See [CHANGELOG.md](CHANGELOG.md) for the tested
scope and [SUPPORT.md](SUPPORT.md) for recovery steps.

## Files and licensing

`skill/` contains the complete four-file skill source. The download contains those
same files with `SKILL.md` at the ZIP root. `downloads/SHA256SUMS` checks the download's
bytes; it is not a UCE evidence check or a signature on a report.

The MCP endpoint is shared with our existing Claude integration. Its hostname
retains `claude`; the service provides the same read-only tools to Gemini. This
repository contains skill and release materials, not a new backend or verifier.

Covered source is available under [MPL-2.0](LICENSE.md). UCE names and marks remain
subject to the separate [trademark notice](NOTICE.md). The skill's license and
notice also travel inside the download.

Operated by **5 Race Street LLC**, under the registered alternate names
**Copyright by UCE** and **CbyUCE**.

[Privacy](https://uceevidencelens.com/gemini/privacy/) · [Terms](https://uceevidencelens.com/gemini/terms/) ·
[Support](https://uceevidencelens.com/gemini/support/) ·
[support@universalcreationevidence.com](mailto:support@universalcreationevidence.com)
