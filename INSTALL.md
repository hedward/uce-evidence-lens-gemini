# Install UCE Evidence Lens for Gemini

Public preview 0.1.0-preview.1 · Instructions checked October 3, 2026.

## 1. Check access

Google currently requires a personal Google Account, age 18+, US location,
English, and Keep Activity enabled for custom connected apps. Check Google's
[current requirements](https://support.google.com/gemini/answer/17209137?hl=en-SM)
and review your privacy choices. If the feature is absent, this package cannot
enable it. Our tested account exposes custom apps in **Spark**; Spark access can
depend on your subscription. Ordinary-chat tools and mobile operation have not
been verified by UCE.

Before connecting, read the [privacy policy](PRIVACY.md) and [terms](TERMS.md).

## 2. Connect the app

In the Gemini web app, open **Settings → Connected Apps**. If needed, open
**Personal Intelligence** first. Under **Custom apps** (or **Custom apps for
Spark**), add:

```text
https://uce-evidence-lens-claude-zptt2ggs7a-uc.a.run.app/mcp
```

Follow Google's connection review. Confirm the app exposes exactly:

- `inspect_uce_record`
- `get_uce_inspection_report`

The service requires no UCE sign-in, API key, or OAuth credentials. If your account
requires credentials for this endpoint or does not discover these tools, stop and
[contact support](SUPPORT.md). Connection approval alone is not a completed check.

## 3. Upload the skill

Download [inspect-uce-evidence.zip](https://github.com/hedward/uce-evidence-lens-gemini/releases/download/v0.1.0-preview.1/inspect-uce-evidence.zip).
In Gemini, choose **Settings → Skills → Upload**, select that ZIP, review it, and
create the skill. Confirm `inspect-uce-evidence` is active.

The ZIP contains instructions, evidence boundaries, and license notices. Upload
this ZIP, not GitHub's automatically generated source-code archive. For Google's
current interface, see [Create and manage skills](https://support.google.com/gemini/answer/17094296?hl=en).

## 4. Inspect a public example

Start a Spark task. Select **UCE Evidence Lens** using `@` and
**inspect-uce-evidence** using `/`, then send:

```text
Inspect this public UCE record:
d16afbafda0ef0bf1be29d4f89e8629fc2aa0eae55da30103aeb5e6a59abd9a5
Explain each check and what remains unsupported or incomplete.
```

Look for an actual UCE tool action and returned check results. A task title or an
empty answer is not an inspection. The result may be partial even when some
integrity checks complete. Review its individual statuses, sources, and limits.

## 5. Request a report

```text
Create an unsigned inspection report for this public UCE record:
d16afbafda0ef0bf1be29d4f89e8629fc2aa0eae55da30103aeb5e6a59abd9a5
Explain what completed and what remains unchecked. Include the exact returned
public-record and Lens viewer URLs as direct links and copyable text.
```

This calls the report tool for a fresh snapshot. It does not create a certificate,
evidence record, or proof of ownership. Native downloadable report attachments
are unverified in this preview. If Gemini supplies complete report JSON, you may
save that JSON yourself; do not treat a prose summary as the original report.

## If a turn is blank

Refresh once to inspect the saved task state, then make one explicit retry using
the same public reference. If it is blank again, stop and use the
[Evidence Lens browser](https://uceevidencelens.com/) or contact support. A missing
response says nothing about whether the record passes or fails a check.

## Update or remove

To update an existing skill, open it and choose **Skill actions → Replace skill**
with the new release ZIP. Keep one active copy. Replacing the skill does not
change the separately connected app. To stop use, deactivate or remove the skill
and disconnect/remove UCE Evidence Lens in Connected Apps. Manage your saved
conversation and task data using Google's account controls.
