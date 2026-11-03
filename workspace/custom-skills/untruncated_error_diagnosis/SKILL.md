# Diagnose from the full error output

## Treat a prefix as no diagnosis

- Do not name a cause from a truncated line or a progress prefix alone.

- Rerun the failing command with full output capture before you report a cause.

- Keep the truncated prefix and the full output as separate records so a later reader can see what was hidden.

- Treat a second identical failure as unproven until the full output for that round has been read.

## Check a helper success claim against its artifact

- Do not accept a success word from a helper as proof that it produced its output.

- Check the artifact the helper was supposed to produce, such as a signature, a cache entry, or a refreshed credential.

- Report the helper as unverified when its success word appears but its artifact is missing or stale.

- Fix the helper claim before you rerun the main command, so the main command does not inherit a false success.

## Recompute a limit check with the platform rule

- Recompute a length or size check with the platform counting rule instead of a plain character count.

- Count every link and media placeholder at the platform counted size when the platform counts them that way.

- Trim the item and recheck the counted size before you retry, when the full output names a limit error.

- Keep the original text in the queue record so a trim never silently replaces the intended item.

## Name the layer only after the full output

- Name the failure layer only from the full output, such as startup, credential acquisition, helper output, or a platform limit.

- Treat a full output that still shows only a progress line as an unproven step, not as a named cause.

- Record the next diagnostic step for an unproven step instead of repeating the same cause report.

- Confirm through a read only check that nothing changed on the platform while the diagnosis was open.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Pause the retry cadence while the full output is still missing, so failed rounds do not pile up behind an unproven cause.

- Ask the user whether a manual route is acceptable while the diagnosis is open, and record any manual result so a later retry does not duplicate it.
