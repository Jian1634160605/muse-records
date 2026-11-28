# Diagnose a failure before retrying

## Get the full output before you name a cause

- Do not name a cause from a truncated line or a progress prefix alone.

- Rerun the failing command with full output capture before you report a cause.

- Keep the truncated prefix and the full output as separate records so a later reader can see what was hidden.

- Treat a second identical failure as unproven until the full output for that round has been read.

- Do not accept a success word from a helper as proof that it produced its output.

- Check the artifact the helper was supposed to produce, such as a signature, a cache entry, or a refreshed credential.

- Report the helper as unverified when its success word appears but its artifact is missing or stale.

- Fix the helper claim before you rerun the main command, so the main command does not inherit a false success.

- Recompute a length or size check with the platform counting rule instead of a plain character count.

- Count every link and media placeholder at the platform counted size when the platform counts them that way.

- Trim the item and recheck the counted size before you retry, when the full output names a limit error.

- Keep the original text in the queue record so a trim never silently replaces the intended item.

- Name the failure layer only from the full output, such as startup, credential acquisition, helper output, or a platform limit.

- Treat a full output that still shows only a progress line as an unproven step, not as a named cause.

- Record the next diagnostic step for an unproven step instead of repeating the same cause report.

- Confirm through a read only check that nothing changed on the platform while the diagnosis was open.

## Stop blind retries after a short run

- Stop scheduled retries after three consecutive failures with the identical init error or the identical platform rejection.

- Hold the queued items in their original order while the client is stuck or the post is rejected.

- Create no duplicate draft for a queued item while its first attempt is still held.

- Resume retries only after a diagnosed change has been made and a read only check has passed.

- Never keep probing the same unchanged draft on a fixed cadence after the stop, since an unchanged draft cannot pass a rejection that already failed three times.

- Pause the retry cadence while the full output is still missing, so failed rounds do not pile up behind an unproven cause.

- Treat a 429 rate limit as a transient limit and retry only after a brief backoff, never as a persistent rejection.

## Diagnose the failing input one at a time

- Treat a failure that happens while the posting client starts up as a client init failure.

- Treat a failure that names a link, text, or media element as rejected or potentially harmful as a platform rejection, not an init failure.

- Record the exact error text and the exit code for every failed attempt.

- Treat an init failure as different from a platform limit unless the error itself names a platform limit code.

- Test the proxy line directly against a public site before you blame the proxy line.

- Check the client session and credential state without printing any credential value.

- Compare the last successful post with the first failed post to find what changed in between.

- For a platform rejection, test the rejected element first by removing or replacing the link, then by shortening the text, and change only one element before each retest.

- Change one input at a time and retest with a read only timeline check before you post again.

- When a service rejects a request by location, check the exit address and the account bound region as separate causes before you blame a VPN or a proxy, and record both results before you name the cause.

- Check the timeline before you judge a round so you know whether the latest post actually changed.

## Verify the result and report an open block

- Confirm a post only when the timeline shows a new post with a new post id and a changed post count.

- Report a still open init failure or a still open platform rejection in the main chat and in the designated urgent channel in the same turn you stop retries.

- Name the platform and the task in the report.

- State the exact error and whether the user must act or you are handling the diagnosis.

- For a rejected link, name the link and ask the user to choose between replacing the link, dropping the link, or pausing the post, and record the choice before any further attempt.

- Ask the user whether a manual post is acceptable while the client is down and record any manual post id so the client does not duplicate it on recovery.

- Pause the retry cadence while the init failure is open instead of letting failed retry jobs pile up.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Start the next diagnosis from the full output record instead of the truncated prefix, so a later round does not repeat the first wrong cause.

- Ask the user whether a manual route is acceptable while the diagnosis is open, and record any manual result so a later retry does not duplicate it.
