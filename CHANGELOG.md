# Release notes

## 0.1.0-preview.1 — October 3, 2026

First public direct-install preview of UCE Evidence Lens for Gemini. Install the
skill ZIP and connect the existing shared UCE MCP endpoint separately. This
release does not create a new backend, change verification behavior, or establish
a Google app-catalog listing.

### Included

- Four-file interpretation skill with evidence boundaries and MPL-2.0 notices.
- Two read-only tools for public-record inspection and fresh unsigned reports.
- Public setup, privacy, terms, support, and versioned download materials.

### Tested scope

In one personal account on the Gemini web app on October 3, 2026:

- The account-free connector discovered both tools.
- Native Spark inspection and report calls succeeded, each after one retry.
- The revised skill asked for a missing reference in ordinary chat without
  selecting a record or calling a verification tool.
- Service-side and packaging tests covered record isolation, source restrictions,
  supported and unsupported formats, tampering, network failures, and archive
  contents. These tests do not prove native Gemini behavior.

### Known limits

Spark also returned blank/failed turns, including on a simple no-tools control.
The cause is not established. Native report downloads, corrected direct source
links, ordinary-chat tool availability, and mobile workflows are unverified.
The tested account offered custom apps in Spark only. Google controls feature
availability and may require a subscription for Spark.

The service hostname retains `claude` because the endpoint is shared. Returned
report schema identifiers may retain `chatgpt` for compatibility; execution context
is server. Neither name changes what was checked or where checks ran.

This preview is suitable for evaluating the supported public-record workflow.
Review the individual checks and their limits before using or resharing results.
